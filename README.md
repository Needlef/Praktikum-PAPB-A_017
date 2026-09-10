# Praktikum PAPB A_017
## Praktikum 2
menggunakan

Box(
modifier = Modifier.fillMaxSize(),
contentAlignment = Alignment.Center
)

agar layout berada di center, yang berisi elemen column

Column(
horizontalAlignment = Alignment.CenterHorizontally,
modifier = Modifier.padding(24.dp).background(
color = Color.LightGray
)
)

Column berfungsi menyimpan seluruh elemen, dan di set warna ligh gray
agar terlihat saja.

Image(
painter = painterResource(id = R.drawable.profil),
contentDescription = "Foto Profil",
modifier = Modifier.size(120.dp).clip(CircleShape).padding(10.dp)
)

Spacer(modifier = Modifier.height(12.dp))

berfungsi untuk menampilkan gambar profil.png yang berada di direktori drawable, dan Spacer memberikan jarak kebawah sebesar 12 dp.

Text("Nama: Bonnie Glenwood", fontSize = 20.sp, fontWeight = FontWeight.Bold)
Spacer(modifier = Modifier.height(12.dp))

Text("Mahasiswa Teknik Informatika")
Spacer(modifier = Modifier.height(12.dp))
FollowButton()

memberikan teks, lalu memanggil fungsi FollowButton()

@Composable
fun FollowButton() {
var isFollowed by remember { mutableStateOf(false) }
Button(onClick = { isFollowed = !isFollowed })  {
Text(if (isFollowed) "Unfollow" else "Follow")
}
}

membuat tombol follow, dengan state default false yang disimpan di variabel isFollowed. jika ditekan maka akan mengganti
text tombolnya menjadi Unfollow, karena isFollowed bernilai true.

