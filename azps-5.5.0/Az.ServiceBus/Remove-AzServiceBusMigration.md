---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
ms.openlocfilehash: 42bb6a61e2298c43cb0828a031495b086b46c9d2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100235700"
---
# <span data-ttu-id="42d2a-101">Remove-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="42d2a-101">Remove-AzServiceBusMigration</span></span>

## <span data-ttu-id="42d2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42d2a-102">SYNOPSIS</span></span>
<span data-ttu-id="42d2a-103">Cmdlet deletes the Migration configuration for Standard to Premium namespaces</span><span class="sxs-lookup"><span data-stu-id="42d2a-103">Cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="42d2a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="42d2a-104">SYNTAX</span></span>

### <span data-ttu-id="42d2a-105">MigrationConfigurationPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="42d2a-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42d2a-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="42d2a-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42d2a-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="42d2a-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42d2a-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="42d2a-108">DESCRIPTION</span></span>
<span data-ttu-id="42d2a-109">С **его учетной записью** удаляется конфигурация миграции для имен Standard в Premium.</span><span class="sxs-lookup"><span data-stu-id="42d2a-109">The **Remove-AzServiceBusMigration** cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="42d2a-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="42d2a-110">EXAMPLES</span></span>

### <span data-ttu-id="42d2a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="42d2a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration
```

<span data-ttu-id="42d2a-112">Удаление конфигурации миграции TestingNamespaceStandardMigration</span><span class="sxs-lookup"><span data-stu-id="42d2a-112">Deletes the 'TestingNamespaceStandardMigration' migration configuration</span></span>

## <span data-ttu-id="42d2a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42d2a-113">PARAMETERS</span></span>

### <span data-ttu-id="42d2a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="42d2a-114">-AsJob</span></span>
<span data-ttu-id="42d2a-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="42d2a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="42d2a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42d2a-116">-DefaultProfile</span></span>
<span data-ttu-id="42d2a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="42d2a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42d2a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42d2a-118">-InputObject</span></span>
<span data-ttu-id="42d2a-119">Service Bus Migration Standard Namespace Object</span><span class="sxs-lookup"><span data-stu-id="42d2a-119">Service Bus Migration Standard Namespace Object</span></span>

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

### <span data-ttu-id="42d2a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="42d2a-120">-Name</span></span>
<span data-ttu-id="42d2a-121">Стандартное имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="42d2a-121">Standard Namespace Name</span></span>

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

### <span data-ttu-id="42d2a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="42d2a-122">-PassThru</span></span>
<span data-ttu-id="42d2a-123">Если эта команда была успешной, ее можно указать как истина.</span><span class="sxs-lookup"><span data-stu-id="42d2a-123">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="42d2a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42d2a-124">-ResourceGroupName</span></span>
<span data-ttu-id="42d2a-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="42d2a-125">Resource Group Name</span></span>

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

### <span data-ttu-id="42d2a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42d2a-126">-ResourceId</span></span>
<span data-ttu-id="42d2a-127">Service Bus Migration Standard Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="42d2a-127">Service Bus Migration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="42d2a-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="42d2a-128">-Confirm</span></span>
<span data-ttu-id="42d2a-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="42d2a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42d2a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42d2a-130">-WhatIf</span></span>
<span data-ttu-id="42d2a-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42d2a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42d2a-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="42d2a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42d2a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42d2a-133">CommonParameters</span></span>
<span data-ttu-id="42d2a-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42d2a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42d2a-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42d2a-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42d2a-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="42d2a-136">INPUTS</span></span>

### <span data-ttu-id="42d2a-137">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="42d2a-137">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="42d2a-138">System.String</span><span class="sxs-lookup"><span data-stu-id="42d2a-138">System.String</span></span>

## <span data-ttu-id="42d2a-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="42d2a-139">OUTPUTS</span></span>

### <span data-ttu-id="42d2a-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="42d2a-140">System.Boolean</span></span>

## <span data-ttu-id="42d2a-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="42d2a-141">NOTES</span></span>

## <span data-ttu-id="42d2a-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="42d2a-142">RELATED LINKS</span></span>
