---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D690C903-A481-45F2-9D42-1CE2F4184A98
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCertificate.md
ms.openlocfilehash: f68a7d29f71d51a25713310a1bf3288df316a34f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733496"
---
# <span data-ttu-id="bf78f-101">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="bf78f-101">Get-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="bf78f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bf78f-102">SYNOPSIS</span></span>
<span data-ttu-id="bf78f-103">Возвращает сертификаты автоматизации.</span><span class="sxs-lookup"><span data-stu-id="bf78f-103">Gets Automation certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf78f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bf78f-104">SYNTAX</span></span>

### <span data-ttu-id="bf78f-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bf78f-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationCertificate [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf78f-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="bf78f-106">ByCertificateName</span></span>
```
Get-AzureRmAutomationCertificate [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf78f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf78f-107">DESCRIPTION</span></span>
<span data-ttu-id="bf78f-108">Командлет **Get-AzureRmAutomationCertificate** получает один или несколько сертификатов Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="bf78f-108">The **Get-AzureRmAutomationCertificate** cmdlet gets one or more Azure Automation certificates.</span></span>
<span data-ttu-id="bf78f-109">По умолчанию этот командлет получает все сертификаты.</span><span class="sxs-lookup"><span data-stu-id="bf78f-109">By default, this cmdlet gets all certificates.</span></span>
<span data-ttu-id="bf78f-110">Укажите имя сертификата для получения определенного сертификата.</span><span class="sxs-lookup"><span data-stu-id="bf78f-110">Specify the name of a certificate to get a specific certificate.</span></span>

## <span data-ttu-id="bf78f-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bf78f-111">EXAMPLES</span></span>

### <span data-ttu-id="bf78f-112">Пример 1: получение всех сертификатов</span><span class="sxs-lookup"><span data-stu-id="bf78f-112">Example 1: Get all certificates</span></span>
```
PS C:\>Get-AzureRmAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="bf78f-113">Эта команда получает метаданные для всех сертификатов в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="bf78f-113">This command gets metadata for all certificates in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="bf78f-114">Пример 2: получение сертификата</span><span class="sxs-lookup"><span data-stu-id="bf78f-114">Example 2: Get a certificate</span></span>
```
PS C:\>Get-AzureRmAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17" -Name "ContosoCertificate"
```

<span data-ttu-id="bf78f-115">Эта команда получает метаданные для сертификата с именем ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="bf78f-115">This command gets metadata for the certificate named ContosoCertificate.</span></span>

## <span data-ttu-id="bf78f-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bf78f-116">PARAMETERS</span></span>

### <span data-ttu-id="bf78f-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bf78f-117">-AutomationAccountName</span></span>
<span data-ttu-id="bf78f-118">Указывает имя учетной записи автоматизации, для которой этот командлет извлекает сертификат.</span><span class="sxs-lookup"><span data-stu-id="bf78f-118">Specifies the name of the Automation account for which this cmdlet retrieves a certificate.</span></span>

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

### <span data-ttu-id="bf78f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf78f-119">-DefaultProfile</span></span>
<span data-ttu-id="bf78f-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bf78f-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bf78f-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bf78f-121">-Name</span></span>
<span data-ttu-id="bf78f-122">Указывает имя извлекаемого сертификата.</span><span class="sxs-lookup"><span data-stu-id="bf78f-122">Specifies the name of a certificate to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf78f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf78f-123">-ResourceGroupName</span></span>
<span data-ttu-id="bf78f-124">Указывает имя группы ресурсов, для которой этот командлет получает сертификат автоматизации.</span><span class="sxs-lookup"><span data-stu-id="bf78f-124">Specifies the name of a resource group for which this cmdlet gets an Automation certificate.</span></span>

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

### <span data-ttu-id="bf78f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf78f-125">CommonParameters</span></span>
<span data-ttu-id="bf78f-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bf78f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf78f-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf78f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf78f-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bf78f-128">INPUTS</span></span>

### <span data-ttu-id="bf78f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="bf78f-129">System.String</span></span>

## <span data-ttu-id="bf78f-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf78f-130">OUTPUTS</span></span>

### <span data-ttu-id="bf78f-131">Microsoft. Azure. Commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="bf78f-131">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="bf78f-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="bf78f-132">NOTES</span></span>

## <span data-ttu-id="bf78f-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bf78f-133">RELATED LINKS</span></span>

[<span data-ttu-id="bf78f-134">New-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="bf78f-134">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="bf78f-135">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="bf78f-135">Remove-AzureRmAutomationCertificate</span></span>](./Remove-AzureRMAutomationCertificate.md)

[<span data-ttu-id="bf78f-136">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="bf78f-136">Set-AzureRmAutomationCertificate</span></span>](./Set-AzureRMAutomationCertificate.md)


