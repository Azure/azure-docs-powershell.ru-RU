---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: FDA8BAAA-7C37-4BCB-9C02-EB6296C09C2B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 00904cc1b67c32bc3658c1c4f6e8b123a5601ff7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076222"
---
# <span data-ttu-id="3b314-101">New-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="3b314-101">New-AzureAutomationCertificate</span></span>

## <span data-ttu-id="3b314-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3b314-102">SYNOPSIS</span></span>

<span data-ttu-id="3b314-103">Создание сертификата службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="3b314-103">Creates an Azure Automation certificate.</span></span>

## <span data-ttu-id="3b314-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3b314-104">SYNTAX</span></span>

```
New-AzureAutomationCertificate -Name <String> [-Description <String>] [-Password <SecureString>] -Path <String>
 [-Exportable] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3b314-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b314-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="3b314-106">Командлет **New-AzureAutomationCertificate** создает сертификат в службе автоматизации Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3b314-106">The **New-AzureAutomationCertificate** cmdlet creates a certificate in Microsoft Azure Automation.</span></span>
<span data-ttu-id="3b314-107">Вы можете указать путь к файлу сертификата для отправки.</span><span class="sxs-lookup"><span data-stu-id="3b314-107">You provide the path to a certificate file to upload.</span></span>

## <span data-ttu-id="3b314-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3b314-108">EXAMPLES</span></span>

### <span data-ttu-id="3b314-109">Пример 1: создание сертификата</span><span class="sxs-lookup"><span data-stu-id="3b314-109">Example 1: Create a certificate</span></span>
```
PS C:\> $password = ConvertTo-SecureString "PassWord!" -AsPlainText -Force
PS C:\> New-AzureAutomationCertificate -AutomationAccountName "Contoso17" -Name "MyCertificate" -Path "./cert.pfx" -Password $password
```

<span data-ttu-id="3b314-110">Эти команды создают сертификат в службе автоматизации Azure с именем MyCertificate.</span><span class="sxs-lookup"><span data-stu-id="3b314-110">These commands create a certificate in Azure Automation named MyCertificate.</span></span>
<span data-ttu-id="3b314-111">Первая команда создает пароль для файла сертификата, который используется во второй команде, создающей сертификат.</span><span class="sxs-lookup"><span data-stu-id="3b314-111">The first command creates the password for the certificate file that is used in the second command that creates the certificate.</span></span>

## <span data-ttu-id="3b314-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3b314-112">PARAMETERS</span></span>

### <span data-ttu-id="3b314-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3b314-113">-AutomationAccountName</span></span>
<span data-ttu-id="3b314-114">Указывает имя учетной записи автоматизации, в которой будет храниться сертификат.</span><span class="sxs-lookup"><span data-stu-id="3b314-114">Specifies the name of the Automation account the certificate will be stored in.</span></span>

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

### <span data-ttu-id="3b314-115">-Описание</span><span class="sxs-lookup"><span data-stu-id="3b314-115">-Description</span></span>
<span data-ttu-id="3b314-116">Задает описание сертификата.</span><span class="sxs-lookup"><span data-stu-id="3b314-116">Specifies a description for the certificate.</span></span>

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

### <span data-ttu-id="3b314-117">-Экспортируемый</span><span class="sxs-lookup"><span data-stu-id="3b314-117">-Exportable</span></span>
<span data-ttu-id="3b314-118">Указывает, что сертификат может быть экспортирован.</span><span class="sxs-lookup"><span data-stu-id="3b314-118">Indicates the certificate can be exported.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b314-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3b314-119">-Name</span></span>
<span data-ttu-id="3b314-120">Задает имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="3b314-120">Specifies a name for the certificate.</span></span>

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

### <span data-ttu-id="3b314-121">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="3b314-121">-Password</span></span>
<span data-ttu-id="3b314-122">Указывает пароль для файла сертификата.</span><span class="sxs-lookup"><span data-stu-id="3b314-122">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="3b314-123">-Path</span><span class="sxs-lookup"><span data-stu-id="3b314-123">-Path</span></span>
<span data-ttu-id="3b314-124">Задает путь к файлу сценария, который нужно отправить.</span><span class="sxs-lookup"><span data-stu-id="3b314-124">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="3b314-125">Файл может представлять собой. cer или. pfx.</span><span class="sxs-lookup"><span data-stu-id="3b314-125">The file can be .cer or .pfx.</span></span>

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

### <span data-ttu-id="3b314-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="3b314-126">-Profile</span></span>
<span data-ttu-id="3b314-127">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3b314-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3b314-128">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3b314-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3b314-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b314-129">CommonParameters</span></span>
<span data-ttu-id="3b314-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3b314-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b314-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b314-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b314-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3b314-132">INPUTS</span></span>

## <span data-ttu-id="3b314-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b314-133">OUTPUTS</span></span>

### <span data-ttu-id="3b314-134">Microsoft. Azure. Commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="3b314-134">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="3b314-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="3b314-135">NOTES</span></span>

## <span data-ttu-id="3b314-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3b314-136">RELATED LINKS</span></span>

[<span data-ttu-id="3b314-137">Get-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="3b314-137">Get-AzureAutomationCertificate</span></span>](./Get-AzureAutomationCertificate.md)

[<span data-ttu-id="3b314-138">Remove-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="3b314-138">Remove-AzureAutomationCertificate</span></span>](./Remove-AzureAutomationCertificate.md)

[<span data-ttu-id="3b314-139">Set-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="3b314-139">Set-AzureAutomationCertificate</span></span>](./Set-AzureAutomationCertificate.md)


