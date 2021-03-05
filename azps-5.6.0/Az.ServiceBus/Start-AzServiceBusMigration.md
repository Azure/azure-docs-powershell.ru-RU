---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/start-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
ms.openlocfilehash: 010e54b21d4abb3068f62e561c002fed6ca734d6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988809"
---
# <span data-ttu-id="b6f6b-101">Start-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="b6f6b-101">Start-AzServiceBusMigration</span></span>

## <span data-ttu-id="b6f6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6f6b-102">SYNOPSIS</span></span>
<span data-ttu-id="b6f6b-103">Создание новой конфигурации миграции и начало переноса сущностями из пространства имен Standard в premium</span><span class="sxs-lookup"><span data-stu-id="b6f6b-103">Creates a new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="b6f6b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b6f6b-104">SYNTAX</span></span>

```
Start-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-TargetNameSpace] <String>
 [-PostMigrationName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b6f6b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6f6b-105">DESCRIPTION</span></span>
<span data-ttu-id="b6f6b-106">Для создания новой конфигурации миграции с **запуском-azServiceBusMigration** запускается перенос сущностями из пространства имен Standard в premium.</span><span class="sxs-lookup"><span data-stu-id="b6f6b-106">The **Start-AzServiceBusMigration** cmdlet creates an new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="b6f6b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b6f6b-107">EXAMPLES</span></span>

### <span data-ttu-id="b6f6b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b6f6b-108">Example 1</span></span>
```powershell
PS C:\> Start-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration -TargetNameSpace /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration -PostMigrationName TestingNamespaceStandardMigrationPostMigration

Name              : TestingNamespaceStandardMigration
Id                : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMigration/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Accepted
TargetNamespace   : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration
PostMigrationName : TestingNamespaceStandardMigrationPostMigration
```

<span data-ttu-id="b6f6b-109">Создает новую конфигурацию миграции для пространства имен TestingNamespaceStandardMigration в области имен TestingNamespacePremiumMigration.</span><span class="sxs-lookup"><span data-stu-id="b6f6b-109">Creates a new migration configuration for 'TestingNamespaceStandardMigration' to 'TestingNamespacePremiumMigration' namespaces</span></span>

## <span data-ttu-id="b6f6b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6f6b-110">PARAMETERS</span></span>

### <span data-ttu-id="b6f6b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6f6b-111">-AsJob</span></span>
<span data-ttu-id="b6f6b-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b6f6b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b6f6b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6f6b-113">-DefaultProfile</span></span>
<span data-ttu-id="b6f6b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b6f6b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6f6b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b6f6b-115">-Name</span></span>
<span data-ttu-id="b6f6b-116">Стандартное имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="b6f6b-116">Standard Namespace Name</span></span>

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

### <span data-ttu-id="b6f6b-117">-PostMigrationName</span><span class="sxs-lookup"><span data-stu-id="b6f6b-117">-PostMigrationName</span></span>
<span data-ttu-id="b6f6b-118">Имя после миграции стандартного пространства имен в миграции</span><span class="sxs-lookup"><span data-stu-id="b6f6b-118">Post Migration Name for Standard Namespace in Migration</span></span>

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

### <span data-ttu-id="b6f6b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6f6b-119">-ResourceGroupName</span></span>
<span data-ttu-id="b6f6b-120">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="b6f6b-120">Resource Group Name</span></span>

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

### <span data-ttu-id="b6f6b-121">-TargetNameSpace</span><span class="sxs-lookup"><span data-stu-id="b6f6b-121">-TargetNameSpace</span></span>
<span data-ttu-id="b6f6b-122">Premium Namespace ARM Id</span><span class="sxs-lookup"><span data-stu-id="b6f6b-122">Premium Namespace ARM Id</span></span>

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

### <span data-ttu-id="b6f6b-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6f6b-123">-Confirm</span></span>
<span data-ttu-id="b6f6b-124">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6f6b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6f6b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6f6b-125">-WhatIf</span></span>
<span data-ttu-id="b6f6b-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6f6b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6f6b-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b6f6b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6f6b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6f6b-128">CommonParameters</span></span>
<span data-ttu-id="b6f6b-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6f6b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6f6b-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6f6b-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6f6b-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b6f6b-131">INPUTS</span></span>

### <span data-ttu-id="b6f6b-132">Нет</span><span class="sxs-lookup"><span data-stu-id="b6f6b-132">None</span></span>

## <span data-ttu-id="b6f6b-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b6f6b-133">OUTPUTS</span></span>

### <span data-ttu-id="b6f6b-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="b6f6b-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="b6f6b-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b6f6b-135">NOTES</span></span>

## <span data-ttu-id="b6f6b-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b6f6b-136">RELATED LINKS</span></span>
