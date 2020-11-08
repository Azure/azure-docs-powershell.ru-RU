---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: AE74024A-A12A-4EC4-AF6C-62F921EA2532
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6b19d0bb0c95e9d489fe26c1cd74705318cedcf2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076428"
---
# <span data-ttu-id="a888d-101">Set-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="a888d-101">Set-AzureAutomationCertificate</span></span>

## <span data-ttu-id="a888d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a888d-102">SYNOPSIS</span></span>

<span data-ttu-id="a888d-103">Изменяет конфигурацию сертификата автоматизации.</span><span class="sxs-lookup"><span data-stu-id="a888d-103">Modifies the configuration of an Automation certificate.</span></span>

## <span data-ttu-id="a888d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a888d-104">SYNTAX</span></span>

```
Set-AzureAutomationCertificate -Name <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="a888d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a888d-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="a888d-106">Командлет **Set-AzureAutomationCertificate** изменяет конфигурацию сертификата в Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="a888d-106">The **Set-AzureAutomationCertificate** cmdlet modifies the configuration of a certificate in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="a888d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a888d-107">EXAMPLES</span></span>

### <span data-ttu-id="a888d-108">Пример 1: обновление сертификата</span><span class="sxs-lookup"><span data-stu-id="a888d-108">Example 1: Update a certificate</span></span>
```
PS C:\> $password = ConvertTo-SecureString "PassWord!" -AsPlainText -Force
PS C:\> Set-AzureAutomationCertificate -AutomationAccountName "Contos17" -Name "MyCertificate" -Path "./cert.pfx" -Password $password
```

<span data-ttu-id="a888d-109">Эти команды обновляют существующий сертификат с именем MyCertificate в автоматизации.</span><span class="sxs-lookup"><span data-stu-id="a888d-109">These commands update an existing certificate named MyCertificate in Automation.</span></span>
<span data-ttu-id="a888d-110">Первая команда создает пароль для файла сертификата, который используется во второй команде, которая обновляет сертификат.</span><span class="sxs-lookup"><span data-stu-id="a888d-110">The first command creates the password for the certificate file that is used in the second command that updates the certificate.</span></span>

## <span data-ttu-id="a888d-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a888d-111">PARAMETERS</span></span>

### <span data-ttu-id="a888d-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a888d-112">-AutomationAccountName</span></span>
<span data-ttu-id="a888d-113">Указывает имя учетной записи автоматизации с помощью сертификата.</span><span class="sxs-lookup"><span data-stu-id="a888d-113">Specifies the name of the Automation account with the certificate.</span></span>

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

### <span data-ttu-id="a888d-114">-Описание</span><span class="sxs-lookup"><span data-stu-id="a888d-114">-Description</span></span>
<span data-ttu-id="a888d-115">Задает описание сертификата.</span><span class="sxs-lookup"><span data-stu-id="a888d-115">Specifies a description for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a888d-116">-Экспортируемый</span><span class="sxs-lookup"><span data-stu-id="a888d-116">-Exportable</span></span>
<span data-ttu-id="a888d-117">Указывает, что сертификат может быть экспортирован.</span><span class="sxs-lookup"><span data-stu-id="a888d-117">Indicates the certificate can be exported.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a888d-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a888d-118">-Name</span></span>
<span data-ttu-id="a888d-119">Указывает имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="a888d-119">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="a888d-120">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="a888d-120">-Password</span></span>
<span data-ttu-id="a888d-121">Указывает пароль для файла сертификата.</span><span class="sxs-lookup"><span data-stu-id="a888d-121">Specifies the password for the certificate file.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a888d-122">-Path</span><span class="sxs-lookup"><span data-stu-id="a888d-122">-Path</span></span>
<span data-ttu-id="a888d-123">Задает путь к файлу сценария, который нужно отправить.</span><span class="sxs-lookup"><span data-stu-id="a888d-123">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="a888d-124">Файл может представлять собой. cer или. pfx.</span><span class="sxs-lookup"><span data-stu-id="a888d-124">The file can be .cer or .pfx.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a888d-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="a888d-125">-Profile</span></span>
<span data-ttu-id="a888d-126">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a888d-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a888d-127">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a888d-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a888d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a888d-128">CommonParameters</span></span>
<span data-ttu-id="a888d-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a888d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a888d-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a888d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a888d-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a888d-131">INPUTS</span></span>

## <span data-ttu-id="a888d-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a888d-132">OUTPUTS</span></span>

### <span data-ttu-id="a888d-133">Microsoft. Azure. Commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="a888d-133">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="a888d-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="a888d-134">NOTES</span></span>

## <span data-ttu-id="a888d-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a888d-135">RELATED LINKS</span></span>

[<span data-ttu-id="a888d-136">Get-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="a888d-136">Get-AzureAutomationCertificate</span></span>](./Get-AzureAutomationCertificate.md)

[<span data-ttu-id="a888d-137">New-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="a888d-137">New-AzureAutomationCertificate</span></span>](./New-AzureAutomationCertificate.md)

[<span data-ttu-id="a888d-138">Remove-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="a888d-138">Remove-AzureAutomationCertificate</span></span>](./Remove-AzureAutomationCertificate.md)


