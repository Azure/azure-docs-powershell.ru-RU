---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A504099E-BA96-45C9-A7A6-195E7087A0D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCertificate.md
ms.openlocfilehash: c80eb16f840fb6d590c139a6ec4b30d73584b741
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100235148"
---
# <span data-ttu-id="4eab3-101">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="4eab3-101">New-AzAutomationCertificate</span></span>

## <span data-ttu-id="4eab3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4eab3-102">SYNOPSIS</span></span>
<span data-ttu-id="4eab3-103">Создает сертификат автоматизации.</span><span class="sxs-lookup"><span data-stu-id="4eab3-103">Creates an Automation certificate.</span></span>

## <span data-ttu-id="4eab3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4eab3-104">SYNTAX</span></span>

```
New-AzAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path] <String> [-Exportable] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4eab3-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4eab3-105">DESCRIPTION</span></span>
<span data-ttu-id="4eab3-106">**Новый-AzAutomationCertificate cmdlet** создает сертификат в автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="4eab3-106">The **New-AzAutomationCertificate** cmdlet creates a certificate in Azure Automation.</span></span>
<span data-ttu-id="4eab3-107">Укаплите путь к файлу сертификата, который нужно отправить.</span><span class="sxs-lookup"><span data-stu-id="4eab3-107">Provide the path to a certificate file to upload.</span></span>

## <span data-ttu-id="4eab3-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4eab3-108">EXAMPLES</span></span>

### <span data-ttu-id="4eab3-109">Пример 1. Создание нового сертификата</span><span class="sxs-lookup"><span data-stu-id="4eab3-109">Example 1: Create a new certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> New-AzAutomationCertificate -AutomationAccountName "Contoso17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="4eab3-110">Первая команда преобразует обычный текст в безопасную строку с помощью ConvertTo-SecureString командлета.</span><span class="sxs-lookup"><span data-stu-id="4eab3-110">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="4eab3-111">Эта команда сохраняет объект в переменной $Password.</span><span class="sxs-lookup"><span data-stu-id="4eab3-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="4eab3-112">Вторая команда создает сертификат с именем ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="4eab3-112">The second command creates a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="4eab3-113">Для этой команды используется пароль, хранимый в $Password.</span><span class="sxs-lookup"><span data-stu-id="4eab3-113">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="4eab3-114">Эта команда определяет имя учетной записи и путь к файлу, который она загружает.</span><span class="sxs-lookup"><span data-stu-id="4eab3-114">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="4eab3-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4eab3-115">PARAMETERS</span></span>

### <span data-ttu-id="4eab3-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4eab3-116">-AutomationAccountName</span></span>
<span data-ttu-id="4eab3-117">Указывает имя учетной записи автоматизации, для которой этот cmdlet хранит сертификат.</span><span class="sxs-lookup"><span data-stu-id="4eab3-117">Specifies the name of the Automation account for which this cmdlet stores the certificate.</span></span>

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

### <span data-ttu-id="4eab3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eab3-118">-DefaultProfile</span></span>
<span data-ttu-id="4eab3-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4eab3-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4eab3-120">-Description</span><span class="sxs-lookup"><span data-stu-id="4eab3-120">-Description</span></span>
<span data-ttu-id="4eab3-121">Описание сертификата.</span><span class="sxs-lookup"><span data-stu-id="4eab3-121">Specifies a description for the certificate.</span></span>

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

### <span data-ttu-id="4eab3-122">-Exportable</span><span class="sxs-lookup"><span data-stu-id="4eab3-122">-Exportable</span></span>
<span data-ttu-id="4eab3-123">Указывает, можно ли экспортировать сертификат.</span><span class="sxs-lookup"><span data-stu-id="4eab3-123">Specifies whether the certificate can be exported.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4eab3-124">-Name</span><span class="sxs-lookup"><span data-stu-id="4eab3-124">-Name</span></span>
<span data-ttu-id="4eab3-125">Указывает имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="4eab3-125">Specifies the name for the certificate.</span></span>

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

### <span data-ttu-id="4eab3-126">-Password</span><span class="sxs-lookup"><span data-stu-id="4eab3-126">-Password</span></span>
<span data-ttu-id="4eab3-127">Пароль для файла сертификата.</span><span class="sxs-lookup"><span data-stu-id="4eab3-127">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="4eab3-128">-Path</span><span class="sxs-lookup"><span data-stu-id="4eab3-128">-Path</span></span>
<span data-ttu-id="4eab3-129">Путь к файлу сценария, который будет добавлен этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4eab3-129">Specifies the path to a script file that this cmdlet uploads.</span></span>
<span data-ttu-id="4eab3-130">Это может быть cer или PFX-файл.</span><span class="sxs-lookup"><span data-stu-id="4eab3-130">The file can be a .cer or a .pfx file.</span></span>

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

### <span data-ttu-id="4eab3-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4eab3-131">-ResourceGroupName</span></span>
<span data-ttu-id="4eab3-132">Имя группы ресурсов, для которой этот cmdlet создает сертификат.</span><span class="sxs-lookup"><span data-stu-id="4eab3-132">Specifies the name of the resource group for which this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="4eab3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eab3-133">CommonParameters</span></span>
<span data-ttu-id="4eab3-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4eab3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eab3-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4eab3-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eab3-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4eab3-136">INPUTS</span></span>

### <span data-ttu-id="4eab3-137">System.String</span><span class="sxs-lookup"><span data-stu-id="4eab3-137">System.String</span></span>

### <span data-ttu-id="4eab3-138">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="4eab3-138">System.Security.SecureString</span></span>

### <span data-ttu-id="4eab3-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4eab3-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4eab3-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4eab3-140">OUTPUTS</span></span>

### <span data-ttu-id="4eab3-141">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="4eab3-141">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="4eab3-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4eab3-142">NOTES</span></span>

<span data-ttu-id="4eab3-143">Эта команда должна запускаться на компьютере, на компьютере, на который вы администратор, а также в сеансе PowerShell с повышенными уровнями. Перед отправкой сертификата этот cmdlet использует локальный хранилище X.509 для извлечения эскиза и клавиши. Если этот cmdlet будет выполниться за пределами сеанса PowerShell с повышенными уровнями, вы получите сообщение об ошибке "Отказано в доступе".</span><span class="sxs-lookup"><span data-stu-id="4eab3-143">This command should be run on a machine that you are an administrator of, as well as in an elevated PowerShell session; before the certificate is uploaded, this cmdlet uses the local X.509 store to retrieve the thumbprint and key, and if this cmdlet is run outside of an elevated PowerShell session, you will receive an "Access denied" error.</span></span>

## <span data-ttu-id="4eab3-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4eab3-144">RELATED LINKS</span></span>

[<span data-ttu-id="4eab3-145">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="4eab3-145">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="4eab3-146">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="4eab3-146">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)

[<span data-ttu-id="4eab3-147">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="4eab3-147">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


