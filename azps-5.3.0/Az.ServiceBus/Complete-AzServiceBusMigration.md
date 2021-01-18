---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/complete-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Complete-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Complete-AzServiceBusMigration.md
ms.openlocfilehash: 883ecf9337cea2b46166b4c1be8625c9763eb7db
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517493"
---
# <span data-ttu-id="7303a-101">Complete-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="7303a-101">Complete-AzServiceBusMigration</span></span>

## <span data-ttu-id="7303a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7303a-102">SYNOPSIS</span></span>
<span data-ttu-id="7303a-103">При настроив переход со стандартного на премиум-пространство имен как завершенный, а строки подключения в стандартном пространстве имен теперь указывают на пространство имен Premium.</span><span class="sxs-lookup"><span data-stu-id="7303a-103">Cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

## <span data-ttu-id="7303a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7303a-104">SYNTAX</span></span>

### <span data-ttu-id="7303a-105">MigrationConfigurationPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7303a-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Complete-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7303a-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7303a-106">NamespaceInputObjectSet</span></span>
```
Complete-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7303a-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7303a-107">NamespaceResourceIdParameterSet</span></span>
```
Complete-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7303a-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7303a-108">DESCRIPTION</span></span>
<span data-ttu-id="7303a-109">С их выполнения можно выполнить переход с стандартного на **премиум-пространство** имен как полный, а строки подключения в стандартном пространстве имен теперь указывают на область имен Premium.</span><span class="sxs-lookup"><span data-stu-id="7303a-109">The **Complete-AzServiceBusMigration** cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

## <span data-ttu-id="7303a-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7303a-110">EXAMPLES</span></span>

### <span data-ttu-id="7303a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7303a-111">Example 1</span></span>
```powershell
PS C:\> Complete-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name NamespaceStandardMigration
```

<span data-ttu-id="7303a-112">Задает полный перенос пространства имен NamespaceStandardMigration.</span><span class="sxs-lookup"><span data-stu-id="7303a-112">Sets the Migration of 'NamespaceStandardMigration' namespace as complete.</span></span>

## <span data-ttu-id="7303a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7303a-113">PARAMETERS</span></span>

### <span data-ttu-id="7303a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7303a-114">-DefaultProfile</span></span>
<span data-ttu-id="7303a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7303a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7303a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7303a-116">-InputObject</span></span>
<span data-ttu-id="7303a-117">Настройка миграции bus службы — стандартный объект Namespace</span><span class="sxs-lookup"><span data-stu-id="7303a-117">Service Bus Migration configuration - Standard Namespace Object</span></span>

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

### <span data-ttu-id="7303a-118">-Name</span><span class="sxs-lookup"><span data-stu-id="7303a-118">-Name</span></span>
<span data-ttu-id="7303a-119">Стандартное имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="7303a-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="7303a-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7303a-120">-PassThru</span></span>
<span data-ttu-id="7303a-121">Если эта команда была успешной, ее можно указать как истина.</span><span class="sxs-lookup"><span data-stu-id="7303a-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="7303a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7303a-122">-ResourceGroupName</span></span>
<span data-ttu-id="7303a-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="7303a-123">Resource Group Name</span></span>

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

### <span data-ttu-id="7303a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7303a-124">-ResourceId</span></span>
<span data-ttu-id="7303a-125">Service Bus Migration — стандартный ИД ресурса пространства имен</span><span class="sxs-lookup"><span data-stu-id="7303a-125">Service Bus Migration - Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="7303a-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7303a-126">-Confirm</span></span>
<span data-ttu-id="7303a-127">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7303a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7303a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7303a-128">-WhatIf</span></span>
<span data-ttu-id="7303a-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7303a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7303a-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7303a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7303a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7303a-131">CommonParameters</span></span>
<span data-ttu-id="7303a-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7303a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7303a-133">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7303a-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7303a-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7303a-134">INPUTS</span></span>

### <span data-ttu-id="7303a-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="7303a-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="7303a-136">System.String</span><span class="sxs-lookup"><span data-stu-id="7303a-136">System.String</span></span>

## <span data-ttu-id="7303a-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7303a-137">OUTPUTS</span></span>

### <span data-ttu-id="7303a-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7303a-138">System.Boolean</span></span>

## <span data-ttu-id="7303a-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7303a-139">NOTES</span></span>

## <span data-ttu-id="7303a-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7303a-140">RELATED LINKS</span></span>
