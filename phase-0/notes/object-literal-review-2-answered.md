[**Back to Home**](./../README.md)

# Object Literal Review 2

## Soal 1
```javascript
/**
 * Kalian ditugaskan untuk membuat sebuah program yang akan dipakai Bandara Internasional Soekarno-Hatta
 * untuk memeriksa apakah seseorang merupakan suspect dari suatu penyakit berbahaya yang baru saja mewabah akhir-akhir ini.
 * Program akan menerima input berupa object yang merepresentasikan penumpang dengan format seperti berikut:
 * 
 *   {
 *     name: (string),
 *     id: (number),
 *     temperature: (number),
 *     travelHistory: [] (array of strings)
 *   }
 * 
 * Program ini akan mengevaluasi apakah seseorang merupakan suspect dari penyakit ini atau tidak, dan menghasilkan output berupa string.
 * Berikut ini adalah kondisi-kondisi yang akan ditangani:
 *   - Jika suhu tubuhnya diatas 35 derajat celcius dan dia pernah mengunjungi salah satu dari 4 negara berikut: 'China', 'Japan', 'Korea', dan 'Singapore', maka dia dinyatakan sebagai "Suspect".
 *   - Jika suhu tubunya tidak diatas 35 derajat celcius, maka dia tidak apa-apa dan dinyatakan "Healthy".
 *       - Namun, jika suhunya tidak diatas 35 derajat celcius tetapi dia pernah berkunjung ke 4 negara diatas, maka dia dinyatakan sebagai seorang "Potential Carrier".
 *   - Jika suhu tubuhnya tinggi tetapi dia tidak pernah berkunjung ke 4 negara tersebut maka dia hanya sakit, dan dinyatakan "Sick".
 *
 * Output yang dikeluarkan program ini memiliki format sebagai berikut:
 *   "Passenger [id] [name] [status]"
 *
 * Status bisa berupa:
 * [status] : Suspect, Healthy, Potential Carrier, Sick
 *
 * RULES
 * - Dilarang menggunakan built-in function kecuali .push()
 */

function evaluatePassenger(passenger) {
  let fever = false;
  let visit = false;

  if (passenger.temperature > 35) {
    fever = true;
  }

  let suspectCountries = ['China', 'Japan', 'Korea', 'Singapore'];
  for (let i = 0; i < suspectCountries.length; i++) {
    for (let j = 0; j < passenger.travelHistory.length; j++) {
      if (suspectCountries[i] === passenger.travelHistory[j]) {
        visit = true;
        break;
      }
    }
  }

  if (fever && visit) {
    return `Passenger ${passenger.id} ${passenger.name} Suspect`;
  } else if (!fever) {
    if (visit) {
      return `Passenger ${passenger.id} ${passenger.name} Potential Carrier`;
    } else {
      return `Passenger ${passenger.id} ${passenger.name} Healthy`;
    }
  } else if (fever && !visit) {
    return `Passenger ${passenger.id} ${passenger.name} Sick`;
  }
}

console.log(evaluatePassenger({ name: 'Budi', id: 50, temperature: 40, travelHistory: ['Russia', 'Japan'] })); //Passenger 50 Budi Suspect
console.log(evaluatePassenger({ name: 'Tono', id: 10, temperature: 40, travelHistory: ['Morocco', 'France', 'Burma'] })); //Passenger 10 Tono Sick
console.log(evaluatePassenger({ name: 'Tsubasa', id: 15, temperature: 30, travelHistory: ['Brazil'] })); //Passenger 15 Tsubasa Healthy
```

## Soal 2

```javascript
/**
 * Buatlah sebuah fungsi yang akan mencocokan requirement dari sebuah perusahaan dengan skill yang dimiliki oleh seseorang.
 * Fungsi ini akan menerima dua parameter yang berupa object.
 *
 * Parameter pertama adalah sebuah object perusahaan dengan beberapa data berikut: nama perusahaan, job yang ditawarkan dan requirement yang dibutuhkan untuk mendapatkan pekerjaan.
 * Parameter kedua adalah sebuah object pelamar dengan beberapa data berikut: nama pelamar, skill pelamar dan job yang dinginkan oleh pelamar tersebut.
 *
 * Fungsi ini akan menghitung persentase kecocokan perusahaan dan pelamar yang dikirimkan dengan beberapa syarat:
 *   1. Jika job yang ditawarkan oleh perusahaan tidak sesuai dengan job yang diinginkan maka persentase mereka adalah 0%.
 *   2. Jika seluruh requirement yang diminta oleh perusahaan dipenuhi oleh pelamar maka persentase mereka adalah 100%.
 *   3. Jika ada beberapa requirement yang tidak dipenuhi pelamar maka persentase akan dihitung dengan rumus:
 *        (jumlah requirement yang dipenuhi) / (requirement yang diminta)
 *      Contoh: Terdapat 3 requirement pada perusahan tetapi pelamar hanya memenuhi 2 requirement.
 *              Maka dari itu persentase pelamar tersebut adalah 66% (pembulatan ke bawah).
 *
 * Jika seseorang mendapatkan persentase diatas 60% maka fungsi akan menghasilkan pesan:
 *   Selamat [nama pelamar], Anda cocok dengan perusahaan [nama perusahaan] dengan persentase kecocokan [persentase]%.
 * Jika tidak, maka fungsi akan menghasilkan pesan:
 *   Mohon maaf [nama pelamar], Anda belum cocok dengan perusaahan [nama perusahaan]. Anda hanya mendapatkan persentase kecocokan [persentase]%.
 */

function companyMatch(company, user) {
  let persentase = 0;
  if (company.job !== user.applyAs) {
    return `Mohon maaf ${user.name}, Anda belum cocok dengan perusaahan ${company.name}. Anda hanya mendapatkan persentase kecocokan ${persentase}%.`
  } else {
    let count = 0;
    for (let i = 0; i < company.requirement.length; i++) {
      for (let j = 0; j < user.skills.length; j++) {
        if (company.requirement[i] === user.skills[i]) {
          count++;
          break;
        }
      }
    }
    persentase = Math.floor(count / company.requirement.length * 100);
    if (persentase > 60) {
      return `Selamat ${user.name}, Anda cocok dengan perusahaan ${company.name} dengan persentase kecocokan ${persentase}%.`;
    } else {
      return `Mohon maaf ${user.name}, Anda belum cocok dengan perusaahan ${company.name}. Anda hanya mendapatkan persentase kecocokan ${persentase}%.`;
    }
  }
}

const company1 = {
  name: 'Pesbok',
  job: 'Frontend Developer',
  requirement: ['HTML', 'CSS', 'JS']
};

const john = {
  name: 'John',
  applyAs: 'Frontend Developer',
  skills: ['HTML', 'CSS', 'JS']
};

const kosasih = {
  name: 'Kosasih',
  applyAs: 'Backend Developer',
  skills: ['Express', 'Node', 'PHP']
};

const marry = {
  name: 'Marry',
  applyAs: 'Frontend Developer',
  skills: ['HTML', 'CSS']
};

console.log(companyMatch(company1, john)); // Selamat John, Anda cocok dengan perusahaan Pesbok dengan persentase kecocokan 100%.
console.log(companyMatch(company1, kosasih)); // Mohon maaf Kosasih, Anda belum cocok dengan perusaahan Pesbok. Anda hanya mendapatkan persentase kecocokan 0%.
console.log(companyMatch(company1, marry)); // Selamat Marry Anda cocok dengan perusahaan Pesbok dengan persentase kecocokan 66%.
```

[**Back to Home**](./../README.md)
