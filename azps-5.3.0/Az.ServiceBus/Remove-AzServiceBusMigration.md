---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
ms.openlocfilehash: 42bb6a61e2298c43cb0828a031495b086b46c9d2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517398"
---
# <span data-ttu-id="7969f-101">Remove-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="7969f-101">Remove-AzServiceBusMigration</span></span>

## <span data-ttu-id="7969f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7969f-102">SYNOPSIS</span></span>
<span data-ttu-id="7969f-103">Cmdlet deletes the Migration configuration for Standard to Premium namespaces</span><span class="sxs-lookup"><span data-stu-id="7969f-103">Cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="7969f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7969f-104">SYNTAX</span></span>

### <span data-ttu-id="7969f-105">MigrationConfigurationPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7969f-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7969f-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7969f-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7969f-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7969f-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7969f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7969f-108">DESCRIPTION</span></span>
<span data-ttu-id="7969f-109">С **его учетной** записью удаляется конфигурация миграции для имен Standard в Premium.</span><span class="sxs-lookup"><span data-stu-id="7969f-109">The **Remove-AzServiceBusMigration** cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="7969f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7969f-110">EXAMPLES</span></span>

### <span data-ttu-id="7969f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7969f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration
```

<span data-ttu-id="7969f-112">Удаление конфигурации миграции TestingNamespaceStandardMigration</span><span class="sxs-lookup"><span data-stu-id="7969f-112">Deletes the 'TestingNamespaceStandardMigration' migration configuration</span></span>

## <span data-ttu-id="7969f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7969f-113">PARAMETERS</span></span>

### <span data-ttu-id="7969f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7969f-114">-AsJob</span></span>
<span data-ttu-id="7969f-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7969f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7969f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7969f-116">-DefaultProfile</span></span>
<span data-ttu-id="7969f-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7969f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7969f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7969f-118">-InputObject</span></span>
<span data-ttu-id="7969f-119">Service Bus Migration Standard Namespace Object</span><span class="sxs-lookup"><span data-stu-id="7969f-119">Service Bus Migration Standard Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7969f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7969f-120">-Name</span></span>
<span data-ttu-id="7969f-121">Стандартное имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="7969f-121">Standard Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7969f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7969f-122">-PassThru</span></span>
<span data-ttu-id="7969f-123">Если эта команда была успешной, ее можно указать как истина.</span><span class="sxs-lookup"><span data-stu-id="7969f-123">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="7969f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7969f-124">-ResourceGroupName</span></span>
<span data-ttu-id="7969f-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="7969f-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7969f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7969f-126">-ResourceId</span></span>
<span data-ttu-id="7969f-127">Service Bus Migration Standard Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="7969f-127">Service Bus Migration Standard Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7969f-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7969f-128">-Confirm</span></span>
<span data-ttu-id="7969f-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7969f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7969f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7969f-130">-WhatIf</span></span>
<span data-ttu-id="7969f-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7969f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7969f-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7969f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7969f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7969f-133">CommonParameters</span></span>
<span data-ttu-id="7969f-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7969f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7969f-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7969f-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7969f-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7969f-136">INPUTS</span></span>

### <span data-ttu-id="7969f-137">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="7969f-137">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="7969f-138">System.String</span><span class="sxs-lookup"><span data-stu-id="7969f-138">System.String</span></span>

## <span data-ttu-id="7969f-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7969f-139">OUTPUTS</span></span>

### <span data-ttu-id="7969f-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7969f-140">System.Boolean</span></span>

## <span data-ttu-id="7969f-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7969f-141">NOTES</span></span>

## <span data-ttu-id="7969f-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7969f-142">RELATED LINKS</span></span>
