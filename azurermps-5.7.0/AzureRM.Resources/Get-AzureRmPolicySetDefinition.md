---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
ms.openlocfilehash: 694f2ef459b50648e934e4ea0e434fe218d4b1f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567410"
---
# <span data-ttu-id="e2a8b-101">Get-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="e2a8b-101">Get-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="e2a8b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e2a8b-102">SYNOPSIS</span></span>
<span data-ttu-id="e2a8b-103">Получение определений политики.</span><span class="sxs-lookup"><span data-stu-id="e2a8b-103">Gets policy set definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2a8b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e2a8b-104">SYNTAX</span></span>

### <span data-ttu-id="e2a8b-105">GetBySubscription (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e2a8b-105">GetBySubscription (Default)</span></span>
```
Get-AzureRmPolicySetDefinition [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e2a8b-106">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e2a8b-106">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmPolicySetDefinition -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2a8b-107">GetById</span><span class="sxs-lookup"><span data-stu-id="e2a8b-107">GetById</span></span>
```
Get-AzureRmPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2a8b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2a8b-108">DESCRIPTION</span></span>
<span data-ttu-id="e2a8b-109">Командлет **Get-AzureRmPolicySetDefinition** получает все определения политики или определенную политику, определяемую именем или идентификатором.</span><span class="sxs-lookup"><span data-stu-id="e2a8b-109">The **Get-AzureRmPolicySetDefinition** cmdlet gets all the policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="e2a8b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e2a8b-110">EXAMPLES</span></span>

### <span data-ttu-id="e2a8b-111">Пример 1: получение определения множества политик</span><span class="sxs-lookup"><span data-stu-id="e2a8b-111">Example 1: Get all policy set definition</span></span>
```
PS C:\>Get-AzureRmPolicySetDefinition
```

<span data-ttu-id="e2a8b-112">Эта команда получает все определения политики.</span><span class="sxs-lookup"><span data-stu-id="e2a8b-112">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="e2a8b-113">Пример 2: получение определения политики по имени</span><span class="sxs-lookup"><span data-stu-id="e2a8b-113">Example 2: Get policy set definition by name</span></span>
```
PS C:\>Get-AzureRmPolicySetDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="e2a8b-114">Эта команда получает определение политики с именем VMPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="e2a8b-114">This command gets the policy set definition named VMPolicyDefinition.</span></span>

## <span data-ttu-id="e2a8b-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e2a8b-115">PARAMETERS</span></span>

### <span data-ttu-id="e2a8b-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e2a8b-116">-ApiVersion</span></span>
<span data-ttu-id="e2a8b-117">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e2a8b-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="e2a8b-118">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="e2a8b-118">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2a8b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2a8b-119">-DefaultProfile</span></span>
<span data-ttu-id="e2a8b-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e2a8b-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2a8b-121">-ID</span><span class="sxs-lookup"><span data-stu-id="e2a8b-121">-Id</span></span>
<span data-ttu-id="e2a8b-122">Полный идентификатор определения политики, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="e2a8b-122">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="e2a8b-123">Например,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="e2a8b-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: GetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2a8b-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e2a8b-124">-Name</span></span>
<span data-ttu-id="e2a8b-125">Имя определения настройки политики.</span><span class="sxs-lookup"><span data-stu-id="e2a8b-125">The policy set definition name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2a8b-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="e2a8b-126">-Pre</span></span>
<span data-ttu-id="e2a8b-127">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="e2a8b-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2a8b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2a8b-128">CommonParameters</span></span>
<span data-ttu-id="e2a8b-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e2a8b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2a8b-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2a8b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2a8b-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e2a8b-131">INPUTS</span></span>

### <span data-ttu-id="e2a8b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e2a8b-132">System.String</span></span>

## <span data-ttu-id="e2a8b-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2a8b-133">OUTPUTS</span></span>

### <span data-ttu-id="e2a8b-134">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="e2a8b-134">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="e2a8b-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="e2a8b-135">NOTES</span></span>

## <span data-ttu-id="e2a8b-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e2a8b-136">RELATED LINKS</span></span>
