---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/start-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
ms.openlocfilehash: 0837532c6e708b4ff7d8cbee4f5ad231b4032347
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242168"
---
# <span data-ttu-id="0c581-101">Start-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="0c581-101">Start-AzServiceBusMigration</span></span>

## <span data-ttu-id="0c581-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c581-102">SYNOPSIS</span></span>
<span data-ttu-id="0c581-103">Создание новой конфигурации миграции и начало переноса сущностями из пространства имен Standard в premium</span><span class="sxs-lookup"><span data-stu-id="0c581-103">Creates a new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="0c581-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0c581-104">SYNTAX</span></span>

```
Start-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-TargetNameSpace] <String>
 [-PostMigrationName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0c581-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c581-105">DESCRIPTION</span></span>
<span data-ttu-id="0c581-106">Для **этого создается** новая конфигурация миграции и начинается перенос сущностями со стандартных на premium.</span><span class="sxs-lookup"><span data-stu-id="0c581-106">The **Start-AzServiceBusMigration** cmdlet creates an new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="0c581-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0c581-107">EXAMPLES</span></span>

### <span data-ttu-id="0c581-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0c581-108">Example 1</span></span>
```powershell
PS C:\> Start-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration -TargetNameSpace /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration -PostMigrationName TestingNamespaceStandardMigrationPostMigration

Name              : TestingNamespaceStandardMigration
Id                : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMigration/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Accepted
TargetNamespace   : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration
PostMigrationName : TestingNamespaceStandardMigrationPostMigration
```

<span data-ttu-id="0c581-109">Создает новую конфигурацию миграции для пространства имен TestingNamespaceStandardMigration в области имен TestingNamespacePremiumMigration.</span><span class="sxs-lookup"><span data-stu-id="0c581-109">Creates a new migration configuration for 'TestingNamespaceStandardMigration' to 'TestingNamespacePremiumMigration' namespaces</span></span>

## <span data-ttu-id="0c581-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c581-110">PARAMETERS</span></span>

### <span data-ttu-id="0c581-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0c581-111">-AsJob</span></span>
<span data-ttu-id="0c581-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="0c581-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0c581-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c581-113">-DefaultProfile</span></span>
<span data-ttu-id="0c581-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0c581-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c581-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0c581-115">-Name</span></span>
<span data-ttu-id="0c581-116">Стандартное имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="0c581-116">Standard Namespace Name</span></span>

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

### <span data-ttu-id="0c581-117">-PostMigrationName</span><span class="sxs-lookup"><span data-stu-id="0c581-117">-PostMigrationName</span></span>
<span data-ttu-id="0c581-118">Имя после миграции стандартного пространства имен в миграции</span><span class="sxs-lookup"><span data-stu-id="0c581-118">Post Migration Name for Standard Namespace in Migration</span></span>

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

### <span data-ttu-id="0c581-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c581-119">-ResourceGroupName</span></span>
<span data-ttu-id="0c581-120">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="0c581-120">Resource Group Name</span></span>

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

### <span data-ttu-id="0c581-121">-TargetNameSpace</span><span class="sxs-lookup"><span data-stu-id="0c581-121">-TargetNameSpace</span></span>
<span data-ttu-id="0c581-122">Premium Namespace ARM Id</span><span class="sxs-lookup"><span data-stu-id="0c581-122">Premium Namespace ARM Id</span></span>

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

### <span data-ttu-id="0c581-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0c581-123">-Confirm</span></span>
<span data-ttu-id="0c581-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="0c581-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c581-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c581-125">-WhatIf</span></span>
<span data-ttu-id="0c581-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c581-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c581-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0c581-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c581-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c581-128">CommonParameters</span></span>
<span data-ttu-id="0c581-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c581-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c581-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c581-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c581-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0c581-131">INPUTS</span></span>

### <span data-ttu-id="0c581-132">Нет</span><span class="sxs-lookup"><span data-stu-id="0c581-132">None</span></span>

## <span data-ttu-id="0c581-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0c581-133">OUTPUTS</span></span>

### <span data-ttu-id="0c581-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="0c581-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="0c581-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0c581-135">NOTES</span></span>

## <span data-ttu-id="0c581-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0c581-136">RELATED LINKS</span></span>
