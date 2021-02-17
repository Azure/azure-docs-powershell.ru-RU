---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/stop-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Stop-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Stop-AzServiceBusMigration.md
ms.openlocfilehash: 615a09d735867d45f9db75ce229d39bc8d9bf75b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100212652"
---
# <span data-ttu-id="e7aca-101">Stop-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="e7aca-101">Stop-AzServiceBusMigration</span></span>

## <span data-ttu-id="e7aca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7aca-102">SYNOPSIS</span></span>
<span data-ttu-id="e7aca-103">{{Fill in the Synopsis}}</span><span class="sxs-lookup"><span data-stu-id="e7aca-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="e7aca-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e7aca-104">SYNTAX</span></span>

### <span data-ttu-id="e7aca-105">MigrationConfigurationPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e7aca-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Stop-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7aca-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e7aca-106">NamespaceInputObjectSet</span></span>
```
Stop-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7aca-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7aca-107">NamespaceResourceIdParameterSet</span></span>
```
Stop-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7aca-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7aca-108">DESCRIPTION</span></span>
<span data-ttu-id="e7aca-109">**Командалеты Stop-AzServiceBusMigration** прервают переход между стандартным и премиум-пространством имен</span><span class="sxs-lookup"><span data-stu-id="e7aca-109">The **Stop-AzServiceBusMigration** cmdlets terminates the Migration between Standard to premium namespace</span></span>

## <span data-ttu-id="e7aca-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e7aca-110">EXAMPLES</span></span>

### <span data-ttu-id="e7aca-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e7aca-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration
```

<span data-ttu-id="e7aca-112">Cmdlet завершает миграцию между стандартным пространством имен и пространством имен Premium, которое предоставляется при создании конфигурации миграции.</span><span class="sxs-lookup"><span data-stu-id="e7aca-112">Cmdlet terminates the migration between Standard namespace and Premium namespace provided while creating the migration configuration.</span></span>

## <span data-ttu-id="e7aca-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7aca-113">PARAMETERS</span></span>

### <span data-ttu-id="e7aca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7aca-114">-DefaultProfile</span></span>
<span data-ttu-id="e7aca-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e7aca-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7aca-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7aca-116">-InputObject</span></span>
<span data-ttu-id="e7aca-117">Объект пространства имен в стандартной конфигурации bus Migration</span><span class="sxs-lookup"><span data-stu-id="e7aca-117">Service Bus Migration Configuration Standard Namespace Object</span></span>

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

### <span data-ttu-id="e7aca-118">-Name</span><span class="sxs-lookup"><span data-stu-id="e7aca-118">-Name</span></span>
<span data-ttu-id="e7aca-119">Стандартное имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="e7aca-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="e7aca-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7aca-120">-PassThru</span></span>
<span data-ttu-id="e7aca-121">Если эта команда была успешной, ее можно указать как истина.</span><span class="sxs-lookup"><span data-stu-id="e7aca-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="e7aca-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7aca-122">-ResourceGroupName</span></span>
<span data-ttu-id="e7aca-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="e7aca-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7aca-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7aca-124">-ResourceId</span></span>
<span data-ttu-id="e7aca-125">Service Bus Migration Configuration Standard Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="e7aca-125">Service Bus Migration Configuration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="e7aca-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e7aca-126">-Confirm</span></span>
<span data-ttu-id="e7aca-127">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e7aca-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7aca-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7aca-128">-WhatIf</span></span>
<span data-ttu-id="e7aca-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7aca-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7aca-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e7aca-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7aca-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7aca-131">CommonParameters</span></span>
<span data-ttu-id="e7aca-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7aca-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7aca-133">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7aca-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7aca-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e7aca-134">INPUTS</span></span>

### <span data-ttu-id="e7aca-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="e7aca-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="e7aca-136">System.String</span><span class="sxs-lookup"><span data-stu-id="e7aca-136">System.String</span></span>

## <span data-ttu-id="e7aca-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e7aca-137">OUTPUTS</span></span>

### <span data-ttu-id="e7aca-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e7aca-138">System.Boolean</span></span>

## <span data-ttu-id="e7aca-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e7aca-139">NOTES</span></span>

## <span data-ttu-id="e7aca-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e7aca-140">RELATED LINKS</span></span>
