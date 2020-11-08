---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A504099E-BA96-45C9-A7A6-195E7087A0D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCertificate.md
ms.openlocfilehash: c80eb16f840fb6d590c139a6ec4b30d73584b741
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074974"
---
# <span data-ttu-id="7f6e1-101">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="7f6e1-101">New-AzAutomationCertificate</span></span>

## <span data-ttu-id="7f6e1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7f6e1-102">SYNOPSIS</span></span>
<span data-ttu-id="7f6e1-103">Создание сертификата автоматизации.</span><span class="sxs-lookup"><span data-stu-id="7f6e1-103">Creates an Automation certificate.</span></span>

## <span data-ttu-id="7f6e1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7f6e1-104">SYNTAX</span></span>

```
New-AzAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path] <String> [-Exportable] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f6e1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f6e1-105">DESCRIPTION</span></span>
<span data-ttu-id="7f6e1-106">Командлет **New-AzAutomationCertificate** создает сертификат в службе автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="7f6e1-106">The **New-AzAutomationCertificate** cmdlet creates a certificate in Azure Automation.</span></span>
<span data-ttu-id="7f6e1-107">Укажите путь к файлу сертификата, который нужно отправить.</span><span class="sxs-lookup"><span data-stu-id="7f6e1-107">Provide the path to a certificate file to upload.</span></span>

## <span data-ttu-id="7f6e1-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7f6e1-108">EXAMPLES</span></span>

### <span data-ttu-id="7f6e1-109">Пример 1: создание нового сертификата</span><span class="sxs-lookup"><span data-stu-id="7f6e1-109">Example 1: Create a new certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> New-AzAutomationCertificate -AutomationAccountName "Contoso17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="7f6e1-110">Первая команда преобразует пароль обычного текста в безопасную строку с помощью командлета ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="7f6e1-110">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="7f6e1-111">Команда сохраняет этот объект в переменной $Password.</span><span class="sxs-lookup"><span data-stu-id="7f6e1-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="7f6e1-112">Вторая команда создает сертификат с именем ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="7f6e1-112">The second command creates a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="7f6e1-113">В команде используется пароль, хранящийся в $Password.</span><span class="sxs-lookup"><span data-stu-id="7f6e1-113">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="7f6e1-114">Команда задает имя учетной записи и путь к файлу, который она отправляет.</span><span class="sxs-lookup"><span data-stu-id="7f6e1-114">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="7f6e1-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7f6e1-115">PARAMETERS</span></span>

### <span data-ttu-id="7f6e1-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7f6e1-116">-AutomationAccountName</span></span>
<span data-ttu-id="7f6e1-117">Указывает имя учетной записи автоматизации, для которой этот командлет хранит сертификат.</span><span class="sxs-lookup"><span data-stu-id="7f6e1-117">Specifies the name of the Automation account for which this cmdlet stores the certificate.</span></span>

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

### <span data-ttu-id="7f6e1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f6e1-118">-DefaultProfile</span></span>
<span data-ttu-id="7f6e1-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7f6e1-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f6e1-120">-Описание</span><span class="sxs-lookup"><span data-stu-id="7f6e1-120">-Description</span></span>
<span data-ttu-id="7f6e1-121">Задает описание сертификата.</span><span class="sxs-lookup"><span data-stu-id="7f6e1-121">Specifies a description for the certificate.</span></span>

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

### <span data-ttu-id="7f6e1-122">-Экспортируемый</span><span class="sxs-lookup"><span data-stu-id="7f6e1-122">-Exportable</span></span>
<span data-ttu-id="7f6e1-123">Указывает, можно ли экспортировать сертификат.</span><span class="sxs-lookup"><span data-stu-id="7f6e1-123">Specifies whether the certificate can be exported.</span></span>

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

### <span data-ttu-id="7f6e1-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7f6e1-124">-Name</span></span>
<span data-ttu-id="7f6e1-125">Задает имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="7f6e1-125">Specifies the name for the certificate.</span></span>

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

### <span data-ttu-id="7f6e1-126">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="7f6e1-126">-Password</span></span>
<span data-ttu-id="7f6e1-127">Указывает пароль для файла сертификата.</span><span class="sxs-lookup"><span data-stu-id="7f6e1-127">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="7f6e1-128">-Path</span><span class="sxs-lookup"><span data-stu-id="7f6e1-128">-Path</span></span>
<span data-ttu-id="7f6e1-129">Задает путь к файлу сценария, который отправляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="7f6e1-129">Specifies the path to a script file that this cmdlet uploads.</span></span>
<span data-ttu-id="7f6e1-130">Файл может быть файлом. cer или. pfx.</span><span class="sxs-lookup"><span data-stu-id="7f6e1-130">The file can be a .cer or a .pfx file.</span></span>

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

### <span data-ttu-id="7f6e1-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f6e1-131">-ResourceGroupName</span></span>
<span data-ttu-id="7f6e1-132">Указывает имя группы ресурсов, для которой этот командлет создает сертификат.</span><span class="sxs-lookup"><span data-stu-id="7f6e1-132">Specifies the name of the resource group for which this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="7f6e1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f6e1-133">CommonParameters</span></span>
<span data-ttu-id="7f6e1-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7f6e1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f6e1-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f6e1-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f6e1-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7f6e1-136">INPUTS</span></span>

### <span data-ttu-id="7f6e1-137">System. String</span><span class="sxs-lookup"><span data-stu-id="7f6e1-137">System.String</span></span>

### <span data-ttu-id="7f6e1-138">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="7f6e1-138">System.Security.SecureString</span></span>

### <span data-ttu-id="7f6e1-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7f6e1-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7f6e1-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f6e1-140">OUTPUTS</span></span>

### <span data-ttu-id="7f6e1-141">Microsoft. Azure. Commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="7f6e1-141">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="7f6e1-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="7f6e1-142">NOTES</span></span>

<span data-ttu-id="7f6e1-143">Эту команду следует выполнять на компьютере, на котором вы являетесь администратором, а также в сеансе с повышенными привилегиями PowerShell; перед отправкой сертификата этот командлет использует локальное хранилище X. 509 для получения отпечатка и ключа, а если этот командлет запущен за пределами сеанса PowerShell с повышенными привилегиями, вы получаете сообщение об ошибке "доступ запрещен".</span><span class="sxs-lookup"><span data-stu-id="7f6e1-143">This command should be run on a machine that you are an administrator of, as well as in an elevated PowerShell session; before the certificate is uploaded, this cmdlet uses the local X.509 store to retrieve the thumbprint and key, and if this cmdlet is run outside of an elevated PowerShell session, you will receive an "Access denied" error.</span></span>

## <span data-ttu-id="7f6e1-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7f6e1-144">RELATED LINKS</span></span>

[<span data-ttu-id="7f6e1-145">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="7f6e1-145">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="7f6e1-146">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="7f6e1-146">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)

[<span data-ttu-id="7f6e1-147">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="7f6e1-147">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


