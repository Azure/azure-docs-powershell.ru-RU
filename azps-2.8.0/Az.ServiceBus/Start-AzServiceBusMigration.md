---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/start-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
ms.openlocfilehash: c01b0e6c940404a37b128572b26749222c82bde0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905321"
---
# <span data-ttu-id="8401e-101">Start-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="8401e-101">Start-AzServiceBusMigration</span></span>

## <span data-ttu-id="8401e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8401e-102">SYNOPSIS</span></span>
<span data-ttu-id="8401e-103">Создание новой конфигурации миграции и начало миграции сущностей из стандартного в расширенное пространство имен</span><span class="sxs-lookup"><span data-stu-id="8401e-103">Creates a new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="8401e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8401e-104">SYNTAX</span></span>

```
Start-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-TargetNameSpace] <String>
 [-PostMigrationName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8401e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8401e-105">DESCRIPTION</span></span>
<span data-ttu-id="8401e-106">Командлет **Start-AzServiceBusMigration** создает новую конфигурацию миграции и начинает миграцию сущностей из стандартных в расширенные пространства имен.</span><span class="sxs-lookup"><span data-stu-id="8401e-106">The **Start-AzServiceBusMigration** cmdlet creates an new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="8401e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8401e-107">EXAMPLES</span></span>

### <span data-ttu-id="8401e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8401e-108">Example 1</span></span>
```powershell
PS C:\> Start-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration -TargetNameSpace /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration -PostMigrationName TestingNamespaceStandardMigrationPostMigration

Name              : TestingNamespaceStandardMigration
Id                : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMigration/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Accepted
TargetNamespace   : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration
PostMigrationName : TestingNamespaceStandardMigrationPostMigration
```

<span data-ttu-id="8401e-109">Создает новую конфигурацию миграции для пространств имен "TestingNamespaceStandardMigration" и "TestingNamespacePremiumMigration"</span><span class="sxs-lookup"><span data-stu-id="8401e-109">Creates a new migration configuration for 'TestingNamespaceStandardMigration' to 'TestingNamespacePremiumMigration' namespaces</span></span>

## <span data-ttu-id="8401e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8401e-110">PARAMETERS</span></span>

### <span data-ttu-id="8401e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8401e-111">-AsJob</span></span>
<span data-ttu-id="8401e-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8401e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8401e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8401e-113">-DefaultProfile</span></span>
<span data-ttu-id="8401e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8401e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8401e-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8401e-115">-Name</span></span>
<span data-ttu-id="8401e-116">Имя стандартного пространства имен</span><span class="sxs-lookup"><span data-stu-id="8401e-116">Standard Namespace Name</span></span>

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

### <span data-ttu-id="8401e-117">-PostMigrationName</span><span class="sxs-lookup"><span data-stu-id="8401e-117">-PostMigrationName</span></span>
<span data-ttu-id="8401e-118">Имя после миграции для стандартного пространства имен в миграции</span><span class="sxs-lookup"><span data-stu-id="8401e-118">Post Migration Name for Standard Namespace in Migration</span></span>

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

### <span data-ttu-id="8401e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8401e-119">-ResourceGroupName</span></span>
<span data-ttu-id="8401e-120">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="8401e-120">Resource Group Name</span></span>

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

### <span data-ttu-id="8401e-121">-TargetNameSpace</span><span class="sxs-lookup"><span data-stu-id="8401e-121">-TargetNameSpace</span></span>
<span data-ttu-id="8401e-122">Идентификатор ARM для пространства имен Premium</span><span class="sxs-lookup"><span data-stu-id="8401e-122">Premium Namespace ARM Id</span></span>

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

### <span data-ttu-id="8401e-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8401e-123">-Confirm</span></span>
<span data-ttu-id="8401e-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8401e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8401e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8401e-125">-WhatIf</span></span>
<span data-ttu-id="8401e-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8401e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8401e-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8401e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8401e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8401e-128">CommonParameters</span></span>
<span data-ttu-id="8401e-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8401e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8401e-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8401e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8401e-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8401e-131">INPUTS</span></span>

### <span data-ttu-id="8401e-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="8401e-132">None</span></span>

## <span data-ttu-id="8401e-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8401e-133">OUTPUTS</span></span>

### <span data-ttu-id="8401e-134">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="8401e-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="8401e-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="8401e-135">NOTES</span></span>

## <span data-ttu-id="8401e-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8401e-136">RELATED LINKS</span></span>
