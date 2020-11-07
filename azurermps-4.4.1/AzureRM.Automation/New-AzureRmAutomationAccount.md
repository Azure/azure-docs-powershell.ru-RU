---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2D5B16F0-0662-4D9F-A13F-808CE5EEBBA3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationAccount.md
ms.openlocfilehash: d40e79e53ccf2ddd9cb5c251328268da0bed76fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732884"
---
# <span data-ttu-id="357be-101">New-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="357be-101">New-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="357be-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="357be-102">SYNOPSIS</span></span>
<span data-ttu-id="357be-103">Создание учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="357be-103">Creates an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="357be-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="357be-104">SYNTAX</span></span>

```
New-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Plan <String>] [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="357be-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="357be-105">DESCRIPTION</span></span>
<span data-ttu-id="357be-106">Командлет **New-AzureRmAutomationAccount** создает учетную запись службы автоматизации Azure в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="357be-106">The **New-AzureRmAutomationAccount** cmdlet creates an Azure Automation account in a resource group.</span></span>

<span data-ttu-id="357be-107">Учетная запись автоматизации является контейнером для ресурсов автоматизации, которые изолированы от ресурсов других учетных записей автоматизации.</span><span class="sxs-lookup"><span data-stu-id="357be-107">An Automation account is a container for Automation resources that is isolated from the resources of other Automation accounts.</span></span> <span data-ttu-id="357be-108">Ресурсы автоматизации включают Runbook, конфигурации необходимой конфигурации состояния (DSC), задания и ресурсы.</span><span class="sxs-lookup"><span data-stu-id="357be-108">Automation resources include runbooks, Desired State Configuration (DSC) configurations, jobs, and assets.</span></span>

## <span data-ttu-id="357be-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="357be-109">EXAMPLES</span></span>

### <span data-ttu-id="357be-110">Пример 1: создание учетной записи автоматизации</span><span class="sxs-lookup"><span data-stu-id="357be-110">Example 1: Create an automation account</span></span>
```
PS C:\> New-AzureRmAutomationAccount -Name "ContosoAutomationAccount" -Location "East US" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="357be-111">Эта команда создает новую учетную запись автоматизации с именем ContosoAutomationAccount в регионе "Восток США".</span><span class="sxs-lookup"><span data-stu-id="357be-111">This command creates a new automation account named ContosoAutomationAccount in the East US region.</span></span>

## <span data-ttu-id="357be-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="357be-112">PARAMETERS</span></span>

### <span data-ttu-id="357be-113">-Location</span><span class="sxs-lookup"><span data-stu-id="357be-113">-Location</span></span>
<span data-ttu-id="357be-114">Указывает расположение, в котором этот командлет создает учетную запись автоматизации.</span><span class="sxs-lookup"><span data-stu-id="357be-114">Specifies the location in which this cmdlet creates the Automation account.</span></span>
<span data-ttu-id="357be-115">Для получения допустимых местоположений используйте командлет Get-AzureRMLocation.</span><span class="sxs-lookup"><span data-stu-id="357be-115">To obtain valid locations, use the Get-AzureRMLocation cmdlet.</span></span>

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

### <span data-ttu-id="357be-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="357be-116">-Name</span></span>
<span data-ttu-id="357be-117">Указывает имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="357be-117">Specifies a name for the Automation account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="357be-118">-Планирование</span><span class="sxs-lookup"><span data-stu-id="357be-118">-Plan</span></span>
<span data-ttu-id="357be-119">Указывает план для учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="357be-119">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="357be-120">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="357be-120">Valid values are:</span></span>

- <span data-ttu-id="357be-121">Базового</span><span class="sxs-lookup"><span data-stu-id="357be-121">Basic</span></span>
- <span data-ttu-id="357be-122">Бесплатно</span><span class="sxs-lookup"><span data-stu-id="357be-122">Free</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="357be-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="357be-123">-ResourceGroupName</span></span>
<span data-ttu-id="357be-124">Указывает имя группы ресурсов, к которой этот командлет добавляет учетную запись автоматизации.</span><span class="sxs-lookup"><span data-stu-id="357be-124">Specifies the name of a resource group to which this cmdlet adds an Automation account.</span></span>

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

### <span data-ttu-id="357be-125">-Теги</span><span class="sxs-lookup"><span data-stu-id="357be-125">-Tags</span></span>
<span data-ttu-id="357be-126">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="357be-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="357be-127">Например:</span><span class="sxs-lookup"><span data-stu-id="357be-127">For example:</span></span>

<span data-ttu-id="357be-128">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="357be-128">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="357be-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="357be-129">-DefaultProfile</span></span>
<span data-ttu-id="357be-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="357be-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="357be-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="357be-131">CommonParameters</span></span>
<span data-ttu-id="357be-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="357be-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="357be-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="357be-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="357be-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="357be-134">INPUTS</span></span>

## <span data-ttu-id="357be-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="357be-135">OUTPUTS</span></span>

### <span data-ttu-id="357be-136">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="357be-136">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="357be-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="357be-137">NOTES</span></span>

## <span data-ttu-id="357be-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="357be-138">RELATED LINKS</span></span>

[<span data-ttu-id="357be-139">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="357be-139">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="357be-140">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="357be-140">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)

[<span data-ttu-id="357be-141">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="357be-141">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)
