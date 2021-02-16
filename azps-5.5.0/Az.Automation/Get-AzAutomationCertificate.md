---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D690C903-A481-45F2-9D42-1CE2F4184A98
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCertificate.md
ms.openlocfilehash: 3a504ba081852ff3bb84a6ace432b394a2b2b478
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100235297"
---
# <span data-ttu-id="28621-101">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="28621-101">Get-AzAutomationCertificate</span></span>

## <span data-ttu-id="28621-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28621-102">SYNOPSIS</span></span>
<span data-ttu-id="28621-103">Получает сертификаты автоматизации.</span><span class="sxs-lookup"><span data-stu-id="28621-103">Gets Automation certificates.</span></span>

## <span data-ttu-id="28621-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="28621-104">SYNTAX</span></span>

### <span data-ttu-id="28621-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="28621-105">ByAll (Default)</span></span>
```
Get-AzAutomationCertificate [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28621-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="28621-106">ByCertificateName</span></span>
```
Get-AzAutomationCertificate [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28621-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="28621-107">DESCRIPTION</span></span>
<span data-ttu-id="28621-108">Чтобы **получить один или** несколько сертификатов автоматизации Azure, можно получить один или несколько сертификатов автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="28621-108">The **Get-AzAutomationCertificate** cmdlet gets one or more Azure Automation certificates.</span></span>
<span data-ttu-id="28621-109">По умолчанию этот cmdlet получает все сертификаты.</span><span class="sxs-lookup"><span data-stu-id="28621-109">By default, this cmdlet gets all certificates.</span></span>
<span data-ttu-id="28621-110">Укажите имя сертификата, чтобы получить определенный сертификат.</span><span class="sxs-lookup"><span data-stu-id="28621-110">Specify the name of a certificate to get a specific certificate.</span></span>

## <span data-ttu-id="28621-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="28621-111">EXAMPLES</span></span>

### <span data-ttu-id="28621-112">Пример 1. Получить все сертификаты</span><span class="sxs-lookup"><span data-stu-id="28621-112">Example 1: Get all certificates</span></span>
```
PS C:\>Get-AzAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="28621-113">Эта команда получает метаданные для всех сертификатов в учетной записи автоматизации Contoso17.</span><span class="sxs-lookup"><span data-stu-id="28621-113">This command gets metadata for all certificates in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="28621-114">Пример 2. Получить сертификат</span><span class="sxs-lookup"><span data-stu-id="28621-114">Example 2: Get a certificate</span></span>
```
PS C:\>Get-AzAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17" -Name "ContosoCertificate"
```

<span data-ttu-id="28621-115">Эта команда получает метаданные для сертификата ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="28621-115">This command gets metadata for the certificate named ContosoCertificate.</span></span>

## <span data-ttu-id="28621-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28621-116">PARAMETERS</span></span>

### <span data-ttu-id="28621-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="28621-117">-AutomationAccountName</span></span>
<span data-ttu-id="28621-118">Указывает имя учетной записи автоматизации, для которой этот cmdlet извлекает сертификат.</span><span class="sxs-lookup"><span data-stu-id="28621-118">Specifies the name of the Automation account for which this cmdlet retrieves a certificate.</span></span>

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

### <span data-ttu-id="28621-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28621-119">-DefaultProfile</span></span>
<span data-ttu-id="28621-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="28621-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="28621-121">-Name</span><span class="sxs-lookup"><span data-stu-id="28621-121">-Name</span></span>
<span data-ttu-id="28621-122">Указывает имя сертификата, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="28621-122">Specifies the name of a certificate to retrieve.</span></span>

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

### <span data-ttu-id="28621-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28621-123">-ResourceGroupName</span></span>
<span data-ttu-id="28621-124">Имя группы ресурсов, для которой этот cmdlet получает сертификат автоматизации.</span><span class="sxs-lookup"><span data-stu-id="28621-124">Specifies the name of a resource group for which this cmdlet gets an Automation certificate.</span></span>

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

### <span data-ttu-id="28621-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28621-125">CommonParameters</span></span>
<span data-ttu-id="28621-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28621-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28621-127">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28621-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28621-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="28621-128">INPUTS</span></span>

### <span data-ttu-id="28621-129">System.String</span><span class="sxs-lookup"><span data-stu-id="28621-129">System.String</span></span>

## <span data-ttu-id="28621-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="28621-130">OUTPUTS</span></span>

### <span data-ttu-id="28621-131">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="28621-131">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="28621-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="28621-132">NOTES</span></span>

## <span data-ttu-id="28621-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="28621-133">RELATED LINKS</span></span>

[<span data-ttu-id="28621-134">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="28621-134">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="28621-135">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="28621-135">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)

[<span data-ttu-id="28621-136">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="28621-136">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


