---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: F1A2861F-14EF-4F67-8452-31FD498528BB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCertificate.md
ms.openlocfilehash: 97a5db6a816b2274befde1d4efb898b0c5e2bfdf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570140"
---
# <span data-ttu-id="91acb-101">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="91acb-101">Set-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="91acb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="91acb-102">SYNOPSIS</span></span>
<span data-ttu-id="91acb-103">Изменяет конфигурацию сертификата автоматизации.</span><span class="sxs-lookup"><span data-stu-id="91acb-103">Modifies the configuration of an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91acb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="91acb-104">SYNTAX</span></span>

```
Set-AzureRmAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91acb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="91acb-105">DESCRIPTION</span></span>
<span data-ttu-id="91acb-106">Командлет **Set-AzureRmAutomationCertificate** изменяет конфигурацию сертификата в Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="91acb-106">The **Set-AzureRmAutomationCertificate** cmdlet modifies the configuration of a certificate in Azure Automation.</span></span>

## <span data-ttu-id="91acb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="91acb-107">EXAMPLES</span></span>

### <span data-ttu-id="91acb-108">Пример 1: изменение сертификата</span><span class="sxs-lookup"><span data-stu-id="91acb-108">Example 1: Modify a certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> Set-AzureAutomationCertificate -AutomationAccountName "Contos17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="91acb-109">Первая команда преобразует пароль обычного текста в безопасную строку с помощью командлета ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="91acb-109">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="91acb-110">Команда сохраняет этот объект в переменной $Password.</span><span class="sxs-lookup"><span data-stu-id="91acb-110">The command stores that object in the $Password variable.</span></span>

<span data-ttu-id="91acb-111">Вторая команда изменяет сертификат с именем ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="91acb-111">The second command modifies a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="91acb-112">В команде используется пароль, хранящийся в $Password.</span><span class="sxs-lookup"><span data-stu-id="91acb-112">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="91acb-113">Команда задает имя учетной записи и путь к файлу, который она отправляет.</span><span class="sxs-lookup"><span data-stu-id="91acb-113">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="91acb-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="91acb-114">PARAMETERS</span></span>

### <span data-ttu-id="91acb-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="91acb-115">-AutomationAccountName</span></span>
<span data-ttu-id="91acb-116">Указывает имя учетной записи автоматизации, для которой этот командлет изменяет сертификат.</span><span class="sxs-lookup"><span data-stu-id="91acb-116">Specifies the name of the Automation account for which this cmdlet modifies a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91acb-117">-Описание</span><span class="sxs-lookup"><span data-stu-id="91acb-117">-Description</span></span>
<span data-ttu-id="91acb-118">Задает описание сертификата, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="91acb-118">Specifies a description for the certificate that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91acb-119">-Экспортируемый</span><span class="sxs-lookup"><span data-stu-id="91acb-119">-Exportable</span></span>
<span data-ttu-id="91acb-120">Указывает, можно ли экспортировать сертификат.</span><span class="sxs-lookup"><span data-stu-id="91acb-120">Specifies whether the certificate can be exported.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91acb-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="91acb-121">-Name</span></span>
<span data-ttu-id="91acb-122">Указывает имя сертификата, который изменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="91acb-122">Specifies the name of the certificate that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91acb-123">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="91acb-123">-Password</span></span>
<span data-ttu-id="91acb-124">Указывает пароль для файла сертификата.</span><span class="sxs-lookup"><span data-stu-id="91acb-124">Specifies the password for the certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91acb-125">-Path</span><span class="sxs-lookup"><span data-stu-id="91acb-125">-Path</span></span>
<span data-ttu-id="91acb-126">Задает путь к файлу сценария, который нужно отправить.</span><span class="sxs-lookup"><span data-stu-id="91acb-126">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="91acb-127">Файл может быть CER-файлом или PFX-файлом.</span><span class="sxs-lookup"><span data-stu-id="91acb-127">The file can be a .cer file or a .pfx file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91acb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91acb-128">-ResourceGroupName</span></span>
<span data-ttu-id="91acb-129">Указывает имя группы ресурсов, для которой этот командлет изменяет сертификат.</span><span class="sxs-lookup"><span data-stu-id="91acb-129">Specifies the name of the resource group for which this cmdlet modifies a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91acb-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91acb-130">-DefaultProfile</span></span>
<span data-ttu-id="91acb-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="91acb-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91acb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91acb-132">CommonParameters</span></span>
<span data-ttu-id="91acb-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="91acb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91acb-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91acb-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91acb-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="91acb-135">INPUTS</span></span>

## <span data-ttu-id="91acb-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="91acb-136">OUTPUTS</span></span>

### <span data-ttu-id="91acb-137">Microsoft. Azure. Commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="91acb-137">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="91acb-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="91acb-138">NOTES</span></span>

## <span data-ttu-id="91acb-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="91acb-139">RELATED LINKS</span></span>

[<span data-ttu-id="91acb-140">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="91acb-140">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="91acb-141">New-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="91acb-141">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="91acb-142">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="91acb-142">Remove-AzureRmAutomationCertificate</span></span>](./Remove-AzureRMAutomationCertificate.md)


