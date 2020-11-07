---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A504099E-BA96-45C9-A7A6-195E7087A0D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCertificate.md
ms.openlocfilehash: 1c3c3cb4fecfde01926e21a75470fc945f8c86c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731570"
---
# <span data-ttu-id="8ac80-101">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="8ac80-101">New-AzAutomationCertificate</span></span>

## <span data-ttu-id="8ac80-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8ac80-102">SYNOPSIS</span></span>
<span data-ttu-id="8ac80-103">Создание сертификата автоматизации.</span><span class="sxs-lookup"><span data-stu-id="8ac80-103">Creates an Automation certificate.</span></span>

## <span data-ttu-id="8ac80-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8ac80-104">SYNTAX</span></span>

```
New-AzAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path] <String> [-Exportable] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ac80-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ac80-105">DESCRIPTION</span></span>
<span data-ttu-id="8ac80-106">Командлет **New-AzAutomationCertificate** создает сертификат в службе автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="8ac80-106">The **New-AzAutomationCertificate** cmdlet creates a certificate in Azure Automation.</span></span>
<span data-ttu-id="8ac80-107">Укажите путь к файлу сертификата, который нужно отправить.</span><span class="sxs-lookup"><span data-stu-id="8ac80-107">Provide the path to a certificate file to upload.</span></span>

## <span data-ttu-id="8ac80-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8ac80-108">EXAMPLES</span></span>

### <span data-ttu-id="8ac80-109">Пример 1: создание нового сертификата</span><span class="sxs-lookup"><span data-stu-id="8ac80-109">Example 1: Create a new certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> New-AzAutomationCertificate -AutomationAccountName "Contoso17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8ac80-110">Первая команда преобразует пароль обычного текста в безопасную строку с помощью командлета ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="8ac80-110">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="8ac80-111">Команда сохраняет этот объект в переменной $Password.</span><span class="sxs-lookup"><span data-stu-id="8ac80-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="8ac80-112">Вторая команда создает сертификат с именем ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="8ac80-112">The second command creates a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="8ac80-113">В команде используется пароль, хранящийся в $Password.</span><span class="sxs-lookup"><span data-stu-id="8ac80-113">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="8ac80-114">Команда задает имя учетной записи и путь к файлу, который она отправляет.</span><span class="sxs-lookup"><span data-stu-id="8ac80-114">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="8ac80-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8ac80-115">PARAMETERS</span></span>

### <span data-ttu-id="8ac80-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8ac80-116">-AutomationAccountName</span></span>
<span data-ttu-id="8ac80-117">Указывает имя учетной записи автоматизации, для которой этот командлет хранит сертификат.</span><span class="sxs-lookup"><span data-stu-id="8ac80-117">Specifies the name of the Automation account for which this cmdlet stores the certificate.</span></span>

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

### <span data-ttu-id="8ac80-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ac80-118">-DefaultProfile</span></span>
<span data-ttu-id="8ac80-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8ac80-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8ac80-120">-Описание</span><span class="sxs-lookup"><span data-stu-id="8ac80-120">-Description</span></span>
<span data-ttu-id="8ac80-121">Задает описание сертификата.</span><span class="sxs-lookup"><span data-stu-id="8ac80-121">Specifies a description for the certificate.</span></span>

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

### <span data-ttu-id="8ac80-122">-Экспортируемый</span><span class="sxs-lookup"><span data-stu-id="8ac80-122">-Exportable</span></span>
<span data-ttu-id="8ac80-123">Указывает, можно ли экспортировать сертификат.</span><span class="sxs-lookup"><span data-stu-id="8ac80-123">Specifies whether the certificate can be exported.</span></span>

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

### <span data-ttu-id="8ac80-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8ac80-124">-Name</span></span>
<span data-ttu-id="8ac80-125">Задает имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="8ac80-125">Specifies the name for the certificate.</span></span>

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

### <span data-ttu-id="8ac80-126">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="8ac80-126">-Password</span></span>
<span data-ttu-id="8ac80-127">Указывает пароль для файла сертификата.</span><span class="sxs-lookup"><span data-stu-id="8ac80-127">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="8ac80-128">-Path</span><span class="sxs-lookup"><span data-stu-id="8ac80-128">-Path</span></span>
<span data-ttu-id="8ac80-129">Задает путь к файлу сценария, который отправляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="8ac80-129">Specifies the path to a script file that this cmdlet uploads.</span></span>
<span data-ttu-id="8ac80-130">Файл может быть файлом. cer или. pfx.</span><span class="sxs-lookup"><span data-stu-id="8ac80-130">The file can be a .cer or a .pfx file.</span></span>

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

### <span data-ttu-id="8ac80-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ac80-131">-ResourceGroupName</span></span>
<span data-ttu-id="8ac80-132">Указывает имя группы ресурсов, для которой этот командлет создает сертификат.</span><span class="sxs-lookup"><span data-stu-id="8ac80-132">Specifies the name of the resource group for which this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="8ac80-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ac80-133">CommonParameters</span></span>
<span data-ttu-id="8ac80-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8ac80-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ac80-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ac80-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ac80-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8ac80-136">INPUTS</span></span>

### <span data-ttu-id="8ac80-137">System. String</span><span class="sxs-lookup"><span data-stu-id="8ac80-137">System.String</span></span>

### <span data-ttu-id="8ac80-138">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="8ac80-138">System.Security.SecureString</span></span>

### <span data-ttu-id="8ac80-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8ac80-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8ac80-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ac80-140">OUTPUTS</span></span>

### <span data-ttu-id="8ac80-141">Microsoft. Azure. Commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="8ac80-141">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="8ac80-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="8ac80-142">NOTES</span></span>

<span data-ttu-id="8ac80-143">Эту команду следует выполнять на компьютере, на котором вы являетесь администратором, а также в сеансе с повышенными привилегиями PowerShell; перед отправкой сертификата этот командлет использует локальное хранилище X. 509 для получения отпечатка и ключа, а если этот командлет запущен за пределами сеанса PowerShell с повышенными привилегиями, вы получаете сообщение об ошибке "доступ запрещен".</span><span class="sxs-lookup"><span data-stu-id="8ac80-143">This command should be run on a machine that you are an administrator of, as well as in an elevated PowerShell session; before the certificate is uploaded, this cmdlet uses the local X.509 store to retrieve the thumbprint and key, and if this cmdlet is run outside of an elevated PowerShell session, you will receive an "Access denied" error.</span></span>

## <span data-ttu-id="8ac80-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8ac80-144">RELATED LINKS</span></span>

[<span data-ttu-id="8ac80-145">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="8ac80-145">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="8ac80-146">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="8ac80-146">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)

[<span data-ttu-id="8ac80-147">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="8ac80-147">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


