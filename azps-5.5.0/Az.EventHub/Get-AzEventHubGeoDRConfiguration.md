---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: 2e324524319a2eacd24bc08aa727892ef08928c0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100220004"
---
# <span data-ttu-id="5df40-101">Get-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="5df40-101">Get-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="5df40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5df40-102">SYNOPSIS</span></span>
<span data-ttu-id="5df40-103">Извлекает псевдоним (конфигурация аварийного восстановления) для основного или дополнительного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="5df40-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="5df40-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5df40-104">SYNTAX</span></span>

### <span data-ttu-id="5df40-105">GeoDRParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5df40-105">GeoDRParameterSet (Default)</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5df40-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5df40-106">NamespaceInputObjectSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5df40-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5df40-107">ResourceIdParameterSet</span></span>
```
Get-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5df40-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5df40-108">DESCRIPTION</span></span>
<span data-ttu-id="5df40-109">The **Get-AzEventHubGeoDRConfiguration** retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span><span class="sxs-lookup"><span data-stu-id="5df40-109">The **Get-AzEventHubGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="5df40-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5df40-110">EXAMPLES</span></span>

### <span data-ttu-id="5df40-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5df40-111">Example 1</span></span>
```
PS C:\> Get-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"

Name              : SampleDRConfigName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRConfigName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
AlternateName     :
Role              : Primary
PendingReplicationOperationsCount : 0
```

<span data-ttu-id="5df40-112">Извлекает псевдоним SampleDRConfigName для основного пространства имен "SampleNamespace_Primary".</span><span class="sxs-lookup"><span data-stu-id="5df40-112">Retrieves alias "SampleDRConfigName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="5df40-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5df40-113">PARAMETERS</span></span>

### <span data-ttu-id="5df40-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5df40-114">-DefaultProfile</span></span>
<span data-ttu-id="5df40-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5df40-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5df40-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5df40-116">-InputObject</span></span>
<span data-ttu-id="5df40-117">Объект Namespace</span><span class="sxs-lookup"><span data-stu-id="5df40-117">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5df40-118">-Name</span><span class="sxs-lookup"><span data-stu-id="5df40-118">-Name</span></span>
<span data-ttu-id="5df40-119">Имя конфигурации DR</span><span class="sxs-lookup"><span data-stu-id="5df40-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="5df40-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5df40-120">-Namespace</span></span>
<span data-ttu-id="5df40-121">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="5df40-121">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5df40-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5df40-122">-ResourceGroupName</span></span>
<span data-ttu-id="5df40-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="5df40-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5df40-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5df40-124">-ResourceId</span></span>
<span data-ttu-id="5df40-125">Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="5df40-125">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5df40-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5df40-126">CommonParameters</span></span>
<span data-ttu-id="5df40-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5df40-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5df40-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5df40-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5df40-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5df40-129">INPUTS</span></span>

### <span data-ttu-id="5df40-130">System.String</span><span class="sxs-lookup"><span data-stu-id="5df40-130">System.String</span></span>

### <span data-ttu-id="5df40-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="5df40-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="5df40-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5df40-132">OUTPUTS</span></span>

### <span data-ttu-id="5df40-133">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="5df40-133">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="5df40-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5df40-134">NOTES</span></span>

## <span data-ttu-id="5df40-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5df40-135">RELATED LINKS</span></span>
