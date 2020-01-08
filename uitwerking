<?php 
//mijn spel aimane chouhaibi
$mijn_hand = '';
$Computer = '';
$resultaat = '';
$result = '';
//me zelf
if (isset($_POST['hand']) === TRUE) {
    $mijn_hand = $_POST['hand'];
    //de tegenstander
    $Computer= strval(mt_rand(0, 2));
    //resultaatt
    $result = result($mijn_hand, $Computer);
}
//resultaat
function result($mijn_hand , $Computer) {
    if ($mijn_hand === $Computer) {
        $result = 'GELIJKSPEL!';
    } elseif (($mijn_hand === '0' && $Computer === '1') || ($mijn_hand === '1' && $Computer === '2') || ($mijn_hand === '2' || $Computer === '0')) {
        $result = 'JE HEBT GEWONNEN!';
    } else {
        $result = 'JE HEBT VERLOREN!';
    }
    return $result;
}
//mijn hand display
function disp_hand(string $hand): string {
    if ($hand === '') {
        return '';
    } elseif ($hand === '0') {
        return 'steen';
    } elseif ($hand === '1') {
        return 'Schaar';
    } else {
        return 'papier';
    }
}
//resulaat 
function e(string $str, string $charset = 'UTF-8'): string {
    return htmlspecialchars($str, ENT_QUOTES | ENT_HTML5, $charset);
}
?>

<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <title>steen papier schaar</title>
</head>
<body>
    <h1>steen papier schaar </h1>
    <p>mijn keuze：<?php print e(disp_hand($mijn_hand)); ?></p>
    <p>tegenstander：<?php print e(disp_hand($Computer));  ?></p>
    <p>resultaat：<?php print e($result); ?></p>
    
    <form method="post">
        
        <label><input type="radio" name="hand" value="0">steen</label>
        <label><input type="radio" name="hand" value="1">schaar</label>
        <label><input type="radio" name="hand" value="2">papier</label>
        <p><input type="submit" value="speel!"></p>
    </form>
</body>
</html>
