---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A504099E-BA96-45C9-A7A6-195E7087A0D4
online version: https://docs.microsoft.com/powershell/module/az.automation/new-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCertificate.md
ms.openlocfilehash: 3f92ebfcb9b768788b0a9acd7a1e11ef766fd22b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010904"
---
# <span data-ttu-id="ac2a2-101">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ac2a2-101">New-AzAutomationCertificate</span></span>

## <span data-ttu-id="ac2a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac2a2-102">SYNOPSIS</span></span>
<span data-ttu-id="ac2a2-103">Создает сертификат автоматизации.</span><span class="sxs-lookup"><span data-stu-id="ac2a2-103">Creates an Automation certificate.</span></span>

## <span data-ttu-id="ac2a2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ac2a2-104">SYNTAX</span></span>

```
New-AzAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path] <String> [-Exportable] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac2a2-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac2a2-105">DESCRIPTION</span></span>
<span data-ttu-id="ac2a2-106">**Новый-AzAutomationCertificate cmdlet** создает сертификат в автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="ac2a2-106">The **New-AzAutomationCertificate** cmdlet creates a certificate in Azure Automation.</span></span>
<span data-ttu-id="ac2a2-107">Укаплите путь к файлу сертификата, который нужно отправить.</span><span class="sxs-lookup"><span data-stu-id="ac2a2-107">Provide the path to a certificate file to upload.</span></span>

## <span data-ttu-id="ac2a2-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ac2a2-108">EXAMPLES</span></span>

### <span data-ttu-id="ac2a2-109">Пример 1. Создание нового сертификата</span><span class="sxs-lookup"><span data-stu-id="ac2a2-109">Example 1: Create a new certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> New-AzAutomationCertificate -AutomationAccountName "Contoso17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ac2a2-110">Первая команда преобразует обычный текст в безопасную строку с помощью ConvertTo-SecureString командлета.</span><span class="sxs-lookup"><span data-stu-id="ac2a2-110">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="ac2a2-111">Эта команда сохраняет объект в переменной $Password.</span><span class="sxs-lookup"><span data-stu-id="ac2a2-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="ac2a2-112">Вторая команда создает сертификат с именем ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="ac2a2-112">The second command creates a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="ac2a2-113">Для этой команды используется пароль, сохраненный в $Password.</span><span class="sxs-lookup"><span data-stu-id="ac2a2-113">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="ac2a2-114">Эта команда определяет имя учетной записи и путь к файлу, который она загружает.</span><span class="sxs-lookup"><span data-stu-id="ac2a2-114">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="ac2a2-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac2a2-115">PARAMETERS</span></span>

### <span data-ttu-id="ac2a2-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ac2a2-116">-AutomationAccountName</span></span>
<span data-ttu-id="ac2a2-117">Указывает имя учетной записи автоматизации, для которой этот cmdlet хранит сертификат.</span><span class="sxs-lookup"><span data-stu-id="ac2a2-117">Specifies the name of the Automation account for which this cmdlet stores the certificate.</span></span>

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

### <span data-ttu-id="ac2a2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac2a2-118">-DefaultProfile</span></span>
<span data-ttu-id="ac2a2-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ac2a2-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ac2a2-120">-Description</span><span class="sxs-lookup"><span data-stu-id="ac2a2-120">-Description</span></span>
<span data-ttu-id="ac2a2-121">Описание сертификата.</span><span class="sxs-lookup"><span data-stu-id="ac2a2-121">Specifies a description for the certificate.</span></span>

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

### <span data-ttu-id="ac2a2-122">-Exportable</span><span class="sxs-lookup"><span data-stu-id="ac2a2-122">-Exportable</span></span>
<span data-ttu-id="ac2a2-123">Указывает, можно ли экспортировать сертификат.</span><span class="sxs-lookup"><span data-stu-id="ac2a2-123">Specifies whether the certificate can be exported.</span></span>

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

### <span data-ttu-id="ac2a2-124">-Name</span><span class="sxs-lookup"><span data-stu-id="ac2a2-124">-Name</span></span>
<span data-ttu-id="ac2a2-125">Указывает имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="ac2a2-125">Specifies the name for the certificate.</span></span>

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

### <span data-ttu-id="ac2a2-126">-Password</span><span class="sxs-lookup"><span data-stu-id="ac2a2-126">-Password</span></span>
<span data-ttu-id="ac2a2-127">Пароль для файла сертификата.</span><span class="sxs-lookup"><span data-stu-id="ac2a2-127">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="ac2a2-128">-Path</span><span class="sxs-lookup"><span data-stu-id="ac2a2-128">-Path</span></span>
<span data-ttu-id="ac2a2-129">Путь к файлу сценария, который будет добавлен этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac2a2-129">Specifies the path to a script file that this cmdlet uploads.</span></span>
<span data-ttu-id="ac2a2-130">Это может быть cer или PFX-файл.</span><span class="sxs-lookup"><span data-stu-id="ac2a2-130">The file can be a .cer or a .pfx file.</span></span>

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

### <span data-ttu-id="ac2a2-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac2a2-131">-ResourceGroupName</span></span>
<span data-ttu-id="ac2a2-132">Имя группы ресурсов, для которой этот cmdlet создает сертификат.</span><span class="sxs-lookup"><span data-stu-id="ac2a2-132">Specifies the name of the resource group for which this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="ac2a2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac2a2-133">CommonParameters</span></span>
<span data-ttu-id="ac2a2-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac2a2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac2a2-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac2a2-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac2a2-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ac2a2-136">INPUTS</span></span>

### <span data-ttu-id="ac2a2-137">System.String</span><span class="sxs-lookup"><span data-stu-id="ac2a2-137">System.String</span></span>

### <span data-ttu-id="ac2a2-138">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="ac2a2-138">System.Security.SecureString</span></span>

### <span data-ttu-id="ac2a2-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ac2a2-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ac2a2-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ac2a2-140">OUTPUTS</span></span>

### <span data-ttu-id="ac2a2-141">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="ac2a2-141">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="ac2a2-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ac2a2-142">NOTES</span></span>

<span data-ttu-id="ac2a2-143">Эта команда должна запускаться на компьютере, на компьютере, на который вы администратор, а также в сеансе PowerShell с повышенными уровнями. перед отправкой сертификата этот cmdlet использует локальный хранилище X.509 для извлечения эскиза и ключа. Если этот cmdlet run outside an elevated PowerShell session, you will receive an "Access denied" (Отказано в доступе).</span><span class="sxs-lookup"><span data-stu-id="ac2a2-143">This command should be run on a machine that you are an administrator of, as well as in an elevated PowerShell session; before the certificate is uploaded, this cmdlet uses the local X.509 store to retrieve the thumbprint and key, and if this cmdlet is run outside of an elevated PowerShell session, you will receive an "Access denied" error.</span></span>

## <span data-ttu-id="ac2a2-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ac2a2-144">RELATED LINKS</span></span>

[<span data-ttu-id="ac2a2-145">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ac2a2-145">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="ac2a2-146">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ac2a2-146">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)

[<span data-ttu-id="ac2a2-147">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ac2a2-147">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


