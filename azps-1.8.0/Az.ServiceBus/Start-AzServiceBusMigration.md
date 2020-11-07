---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/start-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
ms.openlocfilehash: 66d8f15c58d1b4b92f19e23f5940ed7c8ba45d3d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729134"
---
# <span data-ttu-id="f3362-101">Start-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="f3362-101">Start-AzServiceBusMigration</span></span>

## <span data-ttu-id="f3362-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f3362-102">SYNOPSIS</span></span>
<span data-ttu-id="f3362-103">Создание новой конфигурации миграции и начало миграции сущностей из стандартного в расширенное пространство имен</span><span class="sxs-lookup"><span data-stu-id="f3362-103">Creates a new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="f3362-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f3362-104">SYNTAX</span></span>

```
Start-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-TargetNameSpace] <String>
 [-PostMigrationName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f3362-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3362-105">DESCRIPTION</span></span>
<span data-ttu-id="f3362-106">Командлет **Start-AzServiceBusMigration** создает новую конфигурацию миграции и начинает миграцию сущностей из стандартных в расширенные пространства имен.</span><span class="sxs-lookup"><span data-stu-id="f3362-106">The **Start-AzServiceBusMigration** cmdlet creates an new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="f3362-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f3362-107">EXAMPLES</span></span>

### <span data-ttu-id="f3362-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f3362-108">Example 1</span></span>
```powershell
PS C:\> Start-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation -TargetNameSpace /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMirgation -PostMigrationName TestingNamespaceStandardMirgationPostMigration

Name              : TestingNamespaceStandardMirgation
Id                : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMirgation/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Accepted
TargetNamespace   : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMirgation
PostMigrationName : TestingNamespaceStandardMirgationPostMigration
```

<span data-ttu-id="f3362-109">Создает новую конфигурацию миграции для пространств имен "TestingNamespaceStandardMirgation" и "TestingNamespacePremiumMirgation"</span><span class="sxs-lookup"><span data-stu-id="f3362-109">Creates a new migration configuration for 'TestingNamespaceStandardMirgation' to 'TestingNamespacePremiumMirgation' namespaces</span></span>

## <span data-ttu-id="f3362-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f3362-110">PARAMETERS</span></span>

### <span data-ttu-id="f3362-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f3362-111">-AsJob</span></span>
<span data-ttu-id="f3362-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f3362-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3362-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3362-113">-DefaultProfile</span></span>
<span data-ttu-id="f3362-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f3362-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3362-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f3362-115">-Name</span></span>
<span data-ttu-id="f3362-116">Имя стандартного пространства имен</span><span class="sxs-lookup"><span data-stu-id="f3362-116">Standard Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3362-117">-PostMigrationName</span><span class="sxs-lookup"><span data-stu-id="f3362-117">-PostMigrationName</span></span>
<span data-ttu-id="f3362-118">Имя после миграции для пространства имен standrad в миграции</span><span class="sxs-lookup"><span data-stu-id="f3362-118">Post Migration Name for Standrad Namespace in Migration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3362-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3362-119">-ResourceGroupName</span></span>
<span data-ttu-id="f3362-120">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f3362-120">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3362-121">-TargetNameSpace</span><span class="sxs-lookup"><span data-stu-id="f3362-121">-TargetNameSpace</span></span>
<span data-ttu-id="f3362-122">Идентификатор ARM для пространства имен Premium</span><span class="sxs-lookup"><span data-stu-id="f3362-122">Premium Namespace ARM Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3362-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3362-123">-Confirm</span></span>
<span data-ttu-id="f3362-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f3362-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3362-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3362-125">-WhatIf</span></span>
<span data-ttu-id="f3362-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f3362-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3362-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f3362-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3362-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3362-128">CommonParameters</span></span>
<span data-ttu-id="f3362-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f3362-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3362-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3362-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3362-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f3362-131">INPUTS</span></span>

### <span data-ttu-id="f3362-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="f3362-132">None</span></span>

## <span data-ttu-id="f3362-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3362-133">OUTPUTS</span></span>

### <span data-ttu-id="f3362-134">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="f3362-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="f3362-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="f3362-135">NOTES</span></span>

## <span data-ttu-id="f3362-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f3362-136">RELATED LINKS</span></span>
