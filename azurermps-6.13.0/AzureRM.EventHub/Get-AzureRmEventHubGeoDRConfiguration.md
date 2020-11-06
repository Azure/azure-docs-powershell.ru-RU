---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubGeoDRConfiguration.md
ms.openlocfilehash: 40a80a975de56a867f0dcbc34aea0e46d42a155d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563036"
---
# <span data-ttu-id="e4674-101">Get-AzureRmEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4674-101">Get-AzureRmEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="e4674-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e4674-102">SYNOPSIS</span></span>
<span data-ttu-id="e4674-103">Извлекает псевдоним (конфигурацию аварийного восстановления) для основного или дополнительного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="e4674-103">Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4674-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e4674-104">SYNTAX</span></span>

### <span data-ttu-id="e4674-105">GeoDRParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e4674-105">GeoDRParameterSet (Default)</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4674-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e4674-106">NamespaceInputObjectSet</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-InputObject] <PSNamespaceAttributes> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4674-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4674-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmEventHubGeoDRConfiguration [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4674-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e4674-108">DESCRIPTION</span></span>
<span data-ttu-id="e4674-109">Параметр **Get-AzureRmEventHubGeoDRConfiguration** извлекает псевдоним (конфигурацию аварийного восстановления) для основного или дополнительного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="e4674-109">The **Get-AzureRmEventHubGeoDRConfiguration** Retrieves Alias(Disaster Recovery configuration) for primary or secondary namespace</span></span>

## <span data-ttu-id="e4674-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e4674-110">EXAMPLES</span></span>

### <span data-ttu-id="e4674-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e4674-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"

Name              : SampleDRCongifName
Id                : /subscriptions/{SubscriptionId}/resourceGroups/SampleResourceGroup/providers/Microsoft.EventHub/namespaces/SampleNamespace_Primary/disasterRecoveryConfigs/SampleDRCongifName
Type              : Microsoft.EventHub/Namespaces/disasterrecoveryconfigs
ProvisioningState : Accepted
PartnerNamespace  : SampleNamespace_Secondary
AlternateName     :
Role              : Primary
PendingReplicationOperationsCount : 0
```

<span data-ttu-id="e4674-112">Извлекает псевдоним "SampleDRCongifName" для основного пространства имен "SampleNamespace_Primary".</span><span class="sxs-lookup"><span data-stu-id="e4674-112">Retrieves alias "SampleDRCongifName" configuration for primary namespace "SampleNamespace_Primary"</span></span>

## <span data-ttu-id="e4674-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e4674-113">PARAMETERS</span></span>

### <span data-ttu-id="e4674-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4674-114">-DefaultProfile</span></span>
<span data-ttu-id="e4674-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e4674-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4674-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4674-116">-InputObject</span></span>
<span data-ttu-id="e4674-117">Объект Namespace</span><span class="sxs-lookup"><span data-stu-id="e4674-117">Namespace Object</span></span>

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

### <span data-ttu-id="e4674-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e4674-118">-Name</span></span>
<span data-ttu-id="e4674-119">Имя конфигурации DR</span><span class="sxs-lookup"><span data-stu-id="e4674-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="e4674-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e4674-120">-Namespace</span></span>
<span data-ttu-id="e4674-121">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="e4674-121">Namespace Name</span></span>

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

### <span data-ttu-id="e4674-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4674-122">-ResourceGroupName</span></span>
<span data-ttu-id="e4674-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="e4674-123">Resource Group Name</span></span>

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

### <span data-ttu-id="e4674-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4674-124">-ResourceId</span></span>
<span data-ttu-id="e4674-125">Идентификатор ресурса пространства имен</span><span class="sxs-lookup"><span data-stu-id="e4674-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="e4674-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4674-126">CommonParameters</span></span>
<span data-ttu-id="e4674-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e4674-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4674-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4674-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4674-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e4674-129">INPUTS</span></span>

### <span data-ttu-id="e4674-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e4674-130">System.String</span></span>

### <span data-ttu-id="e4674-131">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="e4674-131">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="e4674-132">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e4674-132">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="e4674-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e4674-133">OUTPUTS</span></span>

### <span data-ttu-id="e4674-134">Microsoft. Azure. Commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="e4674-134">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="e4674-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="e4674-135">NOTES</span></span>

## <span data-ttu-id="e4674-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e4674-136">RELATED LINKS</span></span>
