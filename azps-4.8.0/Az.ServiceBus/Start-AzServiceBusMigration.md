---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/start-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
ms.openlocfilehash: 0837532c6e708b4ff7d8cbee4f5ad231b4032347
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077594"
---
# <span data-ttu-id="f2ff5-101">Start-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="f2ff5-101">Start-AzServiceBusMigration</span></span>

## <span data-ttu-id="f2ff5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f2ff5-102">SYNOPSIS</span></span>
<span data-ttu-id="f2ff5-103">Создание новой конфигурации миграции и начало миграции сущностей из стандартного в расширенное пространство имен</span><span class="sxs-lookup"><span data-stu-id="f2ff5-103">Creates a new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="f2ff5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f2ff5-104">SYNTAX</span></span>

```
Start-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-TargetNameSpace] <String>
 [-PostMigrationName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f2ff5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2ff5-105">DESCRIPTION</span></span>
<span data-ttu-id="f2ff5-106">Командлет **Start-AzServiceBusMigration** создает новую конфигурацию миграции и начинает миграцию сущностей из стандартных в расширенные пространства имен.</span><span class="sxs-lookup"><span data-stu-id="f2ff5-106">The **Start-AzServiceBusMigration** cmdlet creates an new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="f2ff5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f2ff5-107">EXAMPLES</span></span>

### <span data-ttu-id="f2ff5-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f2ff5-108">Example 1</span></span>
```powershell
PS C:\> Start-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration -TargetNameSpace /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration -PostMigrationName TestingNamespaceStandardMigrationPostMigration

Name              : TestingNamespaceStandardMigration
Id                : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMigration/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Accepted
TargetNamespace   : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration
PostMigrationName : TestingNamespaceStandardMigrationPostMigration
```

<span data-ttu-id="f2ff5-109">Создает новую конфигурацию миграции для пространств имен "TestingNamespaceStandardMigration" и "TestingNamespacePremiumMigration"</span><span class="sxs-lookup"><span data-stu-id="f2ff5-109">Creates a new migration configuration for 'TestingNamespaceStandardMigration' to 'TestingNamespacePremiumMigration' namespaces</span></span>

## <span data-ttu-id="f2ff5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f2ff5-110">PARAMETERS</span></span>

### <span data-ttu-id="f2ff5-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2ff5-111">-AsJob</span></span>
<span data-ttu-id="f2ff5-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f2ff5-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f2ff5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2ff5-113">-DefaultProfile</span></span>
<span data-ttu-id="f2ff5-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f2ff5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2ff5-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f2ff5-115">-Name</span></span>
<span data-ttu-id="f2ff5-116">Имя стандартного пространства имен</span><span class="sxs-lookup"><span data-stu-id="f2ff5-116">Standard Namespace Name</span></span>

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

### <span data-ttu-id="f2ff5-117">-PostMigrationName</span><span class="sxs-lookup"><span data-stu-id="f2ff5-117">-PostMigrationName</span></span>
<span data-ttu-id="f2ff5-118">Имя после миграции для стандартного пространства имен в миграции</span><span class="sxs-lookup"><span data-stu-id="f2ff5-118">Post Migration Name for Standard Namespace in Migration</span></span>

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

### <span data-ttu-id="f2ff5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2ff5-119">-ResourceGroupName</span></span>
<span data-ttu-id="f2ff5-120">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f2ff5-120">Resource Group Name</span></span>

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

### <span data-ttu-id="f2ff5-121">-TargetNameSpace</span><span class="sxs-lookup"><span data-stu-id="f2ff5-121">-TargetNameSpace</span></span>
<span data-ttu-id="f2ff5-122">Идентификатор ARM для пространства имен Premium</span><span class="sxs-lookup"><span data-stu-id="f2ff5-122">Premium Namespace ARM Id</span></span>

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

### <span data-ttu-id="f2ff5-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f2ff5-123">-Confirm</span></span>
<span data-ttu-id="f2ff5-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f2ff5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2ff5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2ff5-125">-WhatIf</span></span>
<span data-ttu-id="f2ff5-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f2ff5-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2ff5-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f2ff5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2ff5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2ff5-128">CommonParameters</span></span>
<span data-ttu-id="f2ff5-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f2ff5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2ff5-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2ff5-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2ff5-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f2ff5-131">INPUTS</span></span>

### <span data-ttu-id="f2ff5-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="f2ff5-132">None</span></span>

## <span data-ttu-id="f2ff5-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2ff5-133">OUTPUTS</span></span>

### <span data-ttu-id="f2ff5-134">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="f2ff5-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="f2ff5-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="f2ff5-135">NOTES</span></span>

## <span data-ttu-id="f2ff5-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f2ff5-136">RELATED LINKS</span></span>
