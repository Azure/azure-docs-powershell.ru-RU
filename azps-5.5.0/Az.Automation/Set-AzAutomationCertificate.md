---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F1A2861F-14EF-4F67-8452-31FD498528BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCertificate.md
ms.openlocfilehash: 7eaaabf374d4ee9b43477596df06f58593c6d1e9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233681"
---
# <span data-ttu-id="c40ac-101">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="c40ac-101">Set-AzAutomationCertificate</span></span>

## <span data-ttu-id="c40ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c40ac-102">SYNOPSIS</span></span>
<span data-ttu-id="c40ac-103">Изменяет конфигурацию сертификата автоматизации.</span><span class="sxs-lookup"><span data-stu-id="c40ac-103">Modifies the configuration of an Automation certificate.</span></span>

## <span data-ttu-id="c40ac-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c40ac-104">SYNTAX</span></span>

```
Set-AzAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c40ac-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c40ac-105">DESCRIPTION</span></span>
<span data-ttu-id="c40ac-106">**Cmdlet Set-AzAutomationCertificate** изменяет конфигурацию сертификата в автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="c40ac-106">The **Set-AzAutomationCertificate** cmdlet modifies the configuration of a certificate in Azure Automation.</span></span>

## <span data-ttu-id="c40ac-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c40ac-107">EXAMPLES</span></span>

### <span data-ttu-id="c40ac-108">Пример 1. Изменение сертификата</span><span class="sxs-lookup"><span data-stu-id="c40ac-108">Example 1: Modify a certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> Set-AzAutomationCertificate -AutomationAccountName "Contos17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="c40ac-109">Первая команда преобразует обычный текст в безопасную строку с помощью ConvertTo-SecureString командлета.</span><span class="sxs-lookup"><span data-stu-id="c40ac-109">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="c40ac-110">Эта команда сохраняет этот объект в переменной $Password.</span><span class="sxs-lookup"><span data-stu-id="c40ac-110">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="c40ac-111">Вторая команда изменяет сертификат с именем ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="c40ac-111">The second command modifies a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="c40ac-112">Для этой команды используется пароль, сохраненный в $Password.</span><span class="sxs-lookup"><span data-stu-id="c40ac-112">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="c40ac-113">Эта команда определяет имя учетной записи и путь к файлу, который она загружает.</span><span class="sxs-lookup"><span data-stu-id="c40ac-113">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="c40ac-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c40ac-114">PARAMETERS</span></span>

### <span data-ttu-id="c40ac-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c40ac-115">-AutomationAccountName</span></span>
<span data-ttu-id="c40ac-116">Указывает имя учетной записи автоматизации, для которой этот cmdlet изменяет сертификат.</span><span class="sxs-lookup"><span data-stu-id="c40ac-116">Specifies the name of the Automation account for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="c40ac-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c40ac-117">-DefaultProfile</span></span>
<span data-ttu-id="c40ac-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c40ac-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c40ac-119">-Description</span><span class="sxs-lookup"><span data-stu-id="c40ac-119">-Description</span></span>
<span data-ttu-id="c40ac-120">Описание сертификата, который изменяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c40ac-120">Specifies a description for the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c40ac-121">-Exportable</span><span class="sxs-lookup"><span data-stu-id="c40ac-121">-Exportable</span></span>
<span data-ttu-id="c40ac-122">Указывает, можно ли экспортировать сертификат.</span><span class="sxs-lookup"><span data-stu-id="c40ac-122">Specifies whether the certificate can be exported.</span></span>

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

### <span data-ttu-id="c40ac-123">-Name</span><span class="sxs-lookup"><span data-stu-id="c40ac-123">-Name</span></span>
<span data-ttu-id="c40ac-124">Указывает имя сертификата, который изменяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c40ac-124">Specifies the name of the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="c40ac-125">-Password</span><span class="sxs-lookup"><span data-stu-id="c40ac-125">-Password</span></span>
<span data-ttu-id="c40ac-126">Пароль для файла сертификата.</span><span class="sxs-lookup"><span data-stu-id="c40ac-126">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="c40ac-127">-Path</span><span class="sxs-lookup"><span data-stu-id="c40ac-127">-Path</span></span>
<span data-ttu-id="c40ac-128">Путь к файлу сценария, который нужно отправить.</span><span class="sxs-lookup"><span data-stu-id="c40ac-128">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="c40ac-129">Это может быть CER- или PFX-файл.</span><span class="sxs-lookup"><span data-stu-id="c40ac-129">The file can be a .cer file or a .pfx file.</span></span>

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

### <span data-ttu-id="c40ac-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c40ac-130">-ResourceGroupName</span></span>
<span data-ttu-id="c40ac-131">Имя группы ресурсов, для которой этот cmdlet изменяет сертификат.</span><span class="sxs-lookup"><span data-stu-id="c40ac-131">Specifies the name of the resource group for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="c40ac-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c40ac-132">CommonParameters</span></span>
<span data-ttu-id="c40ac-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c40ac-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c40ac-134">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c40ac-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c40ac-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c40ac-135">INPUTS</span></span>

### <span data-ttu-id="c40ac-136">System.String</span><span class="sxs-lookup"><span data-stu-id="c40ac-136">System.String</span></span>

### <span data-ttu-id="c40ac-137">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="c40ac-137">System.Security.SecureString</span></span>

### <span data-ttu-id="c40ac-138">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c40ac-138">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="c40ac-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c40ac-139">OUTPUTS</span></span>

### <span data-ttu-id="c40ac-140">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="c40ac-140">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="c40ac-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c40ac-141">NOTES</span></span>

## <span data-ttu-id="c40ac-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c40ac-142">RELATED LINKS</span></span>

[<span data-ttu-id="c40ac-143">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="c40ac-143">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="c40ac-144">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="c40ac-144">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="c40ac-145">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="c40ac-145">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)


