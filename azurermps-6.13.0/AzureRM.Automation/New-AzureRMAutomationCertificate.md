---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A504099E-BA96-45C9-A7A6-195E7087A0D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCertificate.md
ms.openlocfilehash: 83ec5c8cd9dd9937ca372441d5a9be005bffc76a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563160"
---
# <span data-ttu-id="1e587-101">New-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="1e587-101">New-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="1e587-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1e587-102">SYNOPSIS</span></span>
<span data-ttu-id="1e587-103">Создание сертификата автоматизации.</span><span class="sxs-lookup"><span data-stu-id="1e587-103">Creates an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e587-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1e587-104">SYNTAX</span></span>

```
New-AzureRmAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path] <String> [-Exportable] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e587-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e587-105">DESCRIPTION</span></span>
<span data-ttu-id="1e587-106">Командлет **New-AzureRmAutomationCertificate** создает сертификат в службе автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="1e587-106">The **New-AzureRmAutomationCertificate** cmdlet creates a certificate in Azure Automation.</span></span>
<span data-ttu-id="1e587-107">Укажите путь к файлу сертификата, который нужно отправить.</span><span class="sxs-lookup"><span data-stu-id="1e587-107">Provide the path to a certificate file to upload.</span></span>

## <span data-ttu-id="1e587-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1e587-108">EXAMPLES</span></span>

### <span data-ttu-id="1e587-109">Пример 1: создание нового сертификата</span><span class="sxs-lookup"><span data-stu-id="1e587-109">Example 1: Create a new certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> New-AzureRmAutomationCertificate -AutomationAccountName "Contoso17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="1e587-110">Первая команда преобразует пароль обычного текста в безопасную строку с помощью командлета ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="1e587-110">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="1e587-111">Команда сохраняет этот объект в переменной $Password.</span><span class="sxs-lookup"><span data-stu-id="1e587-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="1e587-112">Вторая команда создает сертификат с именем ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="1e587-112">The second command creates a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="1e587-113">В команде используется пароль, хранящийся в $Password.</span><span class="sxs-lookup"><span data-stu-id="1e587-113">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="1e587-114">Команда задает имя учетной записи и путь к файлу, который она отправляет.</span><span class="sxs-lookup"><span data-stu-id="1e587-114">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="1e587-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1e587-115">PARAMETERS</span></span>

### <span data-ttu-id="1e587-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1e587-116">-AutomationAccountName</span></span>
<span data-ttu-id="1e587-117">Указывает имя учетной записи автоматизации, для которой этот командлет хранит сертификат.</span><span class="sxs-lookup"><span data-stu-id="1e587-117">Specifies the name of the Automation account for which this cmdlet stores the certificate.</span></span>

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

### <span data-ttu-id="1e587-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e587-118">-DefaultProfile</span></span>
<span data-ttu-id="1e587-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1e587-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e587-120">-Описание</span><span class="sxs-lookup"><span data-stu-id="1e587-120">-Description</span></span>
<span data-ttu-id="1e587-121">Задает описание сертификата.</span><span class="sxs-lookup"><span data-stu-id="1e587-121">Specifies a description for the certificate.</span></span>

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

### <span data-ttu-id="1e587-122">-Экспортируемый</span><span class="sxs-lookup"><span data-stu-id="1e587-122">-Exportable</span></span>
<span data-ttu-id="1e587-123">Указывает, можно ли экспортировать сертификат.</span><span class="sxs-lookup"><span data-stu-id="1e587-123">Specifies whether the certificate can be exported.</span></span>

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

### <span data-ttu-id="1e587-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1e587-124">-Name</span></span>
<span data-ttu-id="1e587-125">Задает имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="1e587-125">Specifies the name for the certificate.</span></span>

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

### <span data-ttu-id="1e587-126">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="1e587-126">-Password</span></span>
<span data-ttu-id="1e587-127">Указывает пароль для файла сертификата.</span><span class="sxs-lookup"><span data-stu-id="1e587-127">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="1e587-128">-Path</span><span class="sxs-lookup"><span data-stu-id="1e587-128">-Path</span></span>
<span data-ttu-id="1e587-129">Задает путь к файлу сценария, который отправляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="1e587-129">Specifies the path to a script file that this cmdlet uploads.</span></span>
<span data-ttu-id="1e587-130">Файл может быть файлом. cer или. pfx.</span><span class="sxs-lookup"><span data-stu-id="1e587-130">The file can be a .cer or a .pfx file.</span></span>

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

### <span data-ttu-id="1e587-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e587-131">-ResourceGroupName</span></span>
<span data-ttu-id="1e587-132">Указывает имя группы ресурсов, для которой этот командлет создает сертификат.</span><span class="sxs-lookup"><span data-stu-id="1e587-132">Specifies the name of the resource group for which this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="1e587-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e587-133">CommonParameters</span></span>
<span data-ttu-id="1e587-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1e587-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e587-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e587-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e587-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1e587-136">INPUTS</span></span>

### <span data-ttu-id="1e587-137">System. String</span><span class="sxs-lookup"><span data-stu-id="1e587-137">System.String</span></span>

### <span data-ttu-id="1e587-138">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="1e587-138">System.Security.SecureString</span></span>

### <span data-ttu-id="1e587-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1e587-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1e587-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e587-140">OUTPUTS</span></span>

### <span data-ttu-id="1e587-141">Microsoft. Azure. Commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="1e587-141">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="1e587-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="1e587-142">NOTES</span></span>

## <span data-ttu-id="1e587-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1e587-143">RELATED LINKS</span></span>

[<span data-ttu-id="1e587-144">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="1e587-144">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="1e587-145">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="1e587-145">Remove-AzureRmAutomationCertificate</span></span>](./Remove-AzureRMAutomationCertificate.md)

[<span data-ttu-id="1e587-146">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="1e587-146">Set-AzureRmAutomationCertificate</span></span>](./Set-AzureRMAutomationCertificate.md)


