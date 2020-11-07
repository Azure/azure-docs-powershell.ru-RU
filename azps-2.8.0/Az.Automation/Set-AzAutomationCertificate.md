---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F1A2861F-14EF-4F67-8452-31FD498528BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCertificate.md
ms.openlocfilehash: f300f00558953db00bf99115a9d844b788d1f14a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727741"
---
# <span data-ttu-id="05ca0-101">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="05ca0-101">Set-AzAutomationCertificate</span></span>

## <span data-ttu-id="05ca0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="05ca0-102">SYNOPSIS</span></span>
<span data-ttu-id="05ca0-103">Изменяет конфигурацию сертификата автоматизации.</span><span class="sxs-lookup"><span data-stu-id="05ca0-103">Modifies the configuration of an Automation certificate.</span></span>

## <span data-ttu-id="05ca0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="05ca0-104">SYNTAX</span></span>

```
Set-AzAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05ca0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="05ca0-105">DESCRIPTION</span></span>
<span data-ttu-id="05ca0-106">Командлет **Set-AzAutomationCertificate** изменяет конфигурацию сертификата в Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="05ca0-106">The **Set-AzAutomationCertificate** cmdlet modifies the configuration of a certificate in Azure Automation.</span></span>

## <span data-ttu-id="05ca0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="05ca0-107">EXAMPLES</span></span>

### <span data-ttu-id="05ca0-108">Пример 1: изменение сертификата</span><span class="sxs-lookup"><span data-stu-id="05ca0-108">Example 1: Modify a certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> Set-AzAutomationCertificate -AutomationAccountName "Contos17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="05ca0-109">Первая команда преобразует пароль обычного текста в безопасную строку с помощью командлета ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="05ca0-109">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="05ca0-110">Команда сохраняет этот объект в переменной $Password.</span><span class="sxs-lookup"><span data-stu-id="05ca0-110">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="05ca0-111">Вторая команда изменяет сертификат с именем ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="05ca0-111">The second command modifies a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="05ca0-112">В команде используется пароль, хранящийся в $Password.</span><span class="sxs-lookup"><span data-stu-id="05ca0-112">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="05ca0-113">Команда задает имя учетной записи и путь к файлу, который она отправляет.</span><span class="sxs-lookup"><span data-stu-id="05ca0-113">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="05ca0-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="05ca0-114">PARAMETERS</span></span>

### <span data-ttu-id="05ca0-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="05ca0-115">-AutomationAccountName</span></span>
<span data-ttu-id="05ca0-116">Указывает имя учетной записи автоматизации, для которой этот командлет изменяет сертификат.</span><span class="sxs-lookup"><span data-stu-id="05ca0-116">Specifies the name of the Automation account for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="05ca0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05ca0-117">-DefaultProfile</span></span>
<span data-ttu-id="05ca0-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="05ca0-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05ca0-119">-Описание</span><span class="sxs-lookup"><span data-stu-id="05ca0-119">-Description</span></span>
<span data-ttu-id="05ca0-120">Задает описание сертификата, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="05ca0-120">Specifies a description for the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="05ca0-121">-Экспортируемый</span><span class="sxs-lookup"><span data-stu-id="05ca0-121">-Exportable</span></span>
<span data-ttu-id="05ca0-122">Указывает, можно ли экспортировать сертификат.</span><span class="sxs-lookup"><span data-stu-id="05ca0-122">Specifies whether the certificate can be exported.</span></span>

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

### <span data-ttu-id="05ca0-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="05ca0-123">-Name</span></span>
<span data-ttu-id="05ca0-124">Указывает имя сертификата, который изменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="05ca0-124">Specifies the name of the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="05ca0-125">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="05ca0-125">-Password</span></span>
<span data-ttu-id="05ca0-126">Указывает пароль для файла сертификата.</span><span class="sxs-lookup"><span data-stu-id="05ca0-126">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="05ca0-127">-Path</span><span class="sxs-lookup"><span data-stu-id="05ca0-127">-Path</span></span>
<span data-ttu-id="05ca0-128">Задает путь к файлу сценария, который нужно отправить.</span><span class="sxs-lookup"><span data-stu-id="05ca0-128">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="05ca0-129">Файл может быть CER-файлом или PFX-файлом.</span><span class="sxs-lookup"><span data-stu-id="05ca0-129">The file can be a .cer file or a .pfx file.</span></span>

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

### <span data-ttu-id="05ca0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05ca0-130">-ResourceGroupName</span></span>
<span data-ttu-id="05ca0-131">Указывает имя группы ресурсов, для которой этот командлет изменяет сертификат.</span><span class="sxs-lookup"><span data-stu-id="05ca0-131">Specifies the name of the resource group for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="05ca0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05ca0-132">CommonParameters</span></span>
<span data-ttu-id="05ca0-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="05ca0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05ca0-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05ca0-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05ca0-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="05ca0-135">INPUTS</span></span>

### <span data-ttu-id="05ca0-136">System. String</span><span class="sxs-lookup"><span data-stu-id="05ca0-136">System.String</span></span>

### <span data-ttu-id="05ca0-137">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="05ca0-137">System.Security.SecureString</span></span>

### <span data-ttu-id="05ca0-138">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="05ca0-138">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="05ca0-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="05ca0-139">OUTPUTS</span></span>

### <span data-ttu-id="05ca0-140">Microsoft. Azure. Commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="05ca0-140">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="05ca0-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="05ca0-141">NOTES</span></span>

## <span data-ttu-id="05ca0-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="05ca0-142">RELATED LINKS</span></span>

[<span data-ttu-id="05ca0-143">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="05ca0-143">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="05ca0-144">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="05ca0-144">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="05ca0-145">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="05ca0-145">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)


