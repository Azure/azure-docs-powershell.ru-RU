---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVpnClientRootCertificate.md
ms.openlocfilehash: bd260deb8e43450b2feacb3c60f34ed6cc4003be
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909598"
---
# New-AzVpnClientRootCertificate

## КРАТКИй обзор
Создание нового корневого сертификата VPN-клиента.

## Максимальное

```
New-AzVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzVpnClientRootCertificate** создает новый корневой сертификат VPN для использования на шлюзе виртуальной сети.
Корневые сертификаты — это сертификаты X. 509, определяющие корневой центр сертификации: все остальные сертификаты, используемые в доверенном шлюзе, — это корневой сертификат.

Этот командлет создает изолированный сертификат, не назначенный виртуальному шлюзу.
Вместо этого сертификат, созданный с помощью **New-AzVpnClientRootCertificate** , используется вместе с командлетом New-AzVirtualNetworkGateway при создании нового шлюза.
Например, предположим, что вы создали новый сертификат и хотите сохранить его в переменной с именем $Certificate.
Затем вы можете использовать этот объект сертификата при создании нового виртуального шлюза.
Например,

`New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`

Дополнительные сведения можно найти в документации по командлету New-AzVirtualNetworkGateway.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание корневого сертификата aclient
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

В этом примере создается корневой сертификат клиента и сохраняется объект сертификата в переменной с именем $Certificate.
Эта переменная может затем использоваться командлетом **New-AzVirtualNetworkGateway** для добавления корневого сертификата в новый шлюз виртуальной сети.

Первая команда использует командлет **Get-Content** для получения предварительно экспортированного текстового представления корневого сертификата; текстовые данные хранятся в переменной с именем $Text.

Вторая команда использует цикл for, чтобы извлечь весь текст, кроме первой строки и последней строки, сохранив извлеченный текст в переменной с именем $CertificateText.

Третья команда использует командлет **New-AzVpnClientRootCertificate** , чтобы создать сертификат, сохранив созданный объект в переменной с именем $Certificate.

## ПАРАМЕТРЫ

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (имя)
Указывает имя для нового корневого сертификата клиента.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicCertData
Указывает текстовое представление корневого сертификата, который нужно добавить.
Чтобы получить текстовое представление, экспортируйте его в формате CER (с помощью кодировки Base64), а затем откройте полученный файл в текстовом редакторе.
На экран будет выведено сообщение (Обратите внимание на то, что реальный вывод содержит гораздо больше строк, чем сокращенный образец, показанный ниже).

-----"Начало-----сертификата" MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----конец сертификата-----

PublicCertData состоит из всех строк между первой строкой (-----"начало-----сертификата") и последней строки (-----конец сертификата-----) в файле.
Вы можете получить PublicCertData с помощью команд Windows PowerShell, как показано ниже:

$Text = Get-Content-Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = для ($i = 1; $i-lt $Text. length-1; $i + +) {$Text \[ $i \] }

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

###  
Этот командлет не поддерживает конвейерный вход.

## НАПРЯЖЕНИЕ

###  
Этот командлет создает новые экземпляры объекта **Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate** .

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Add-AzVpnClientRootCertificate](./Add-AzVpnClientRootCertificate.md)

[Get-AzVpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[Remove-AzVpnClientRootCertificate](./Remove-AzVpnClientRootCertificate.md)


