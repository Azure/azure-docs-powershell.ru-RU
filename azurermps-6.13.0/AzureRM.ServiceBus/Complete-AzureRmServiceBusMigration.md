---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/complete-azurermservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Complete-AzureRmServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Complete-AzureRmServiceBusMigration.md
ms.openlocfilehash: 0006e4768dc27994d18e93e48696b5ee9a514c45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733799"
---
# <span data-ttu-id="ea7ca-101">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="ea7ca-101">Complete-AzureRmServiceBusMigration</span></span>

## <span data-ttu-id="ea7ca-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ea7ca-102">SYNOPSIS</span></span>
<span data-ttu-id="ea7ca-103">Командлеты устанавливают переход с Standard на Premium Namespace как завершенные и строки подключения в стандартном пространстве имен теперь указывают на пространство имен Premium.</span><span class="sxs-lookup"><span data-stu-id="ea7ca-103">Cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea7ca-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ea7ca-104">SYNTAX</span></span>

### <span data-ttu-id="ea7ca-105">MigrationConfigurationPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ea7ca-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Complete-AzureRmServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea7ca-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ea7ca-106">NamespaceInputObjectSet</span></span>
```
Complete-AzureRmServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea7ca-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea7ca-107">NamespaceResourceIdParameterSet</span></span>
```
Complete-AzureRmServiceBusMigration [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea7ca-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea7ca-108">DESCRIPTION</span></span>
<span data-ttu-id="ea7ca-109">Командлеты **Complete-AzureRmServiceBusMigration** устанавливают переход от стандартного к расширенному пространству имен как завершенные и строки подключения в стандартном пространстве имен теперь указывают на пространство имен Premium.</span><span class="sxs-lookup"><span data-stu-id="ea7ca-109">The **Complete-AzureRmServiceBusMigration** cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

## <span data-ttu-id="ea7ca-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ea7ca-110">EXAMPLES</span></span>

### <span data-ttu-id="ea7ca-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ea7ca-111">Example 1</span></span>
```powershell
PS C:\> Complete-AzureRmServiceBusMigration -ResourceGroupName ResourceGroup -Name NamespaceStandardMirgation
```

<span data-ttu-id="ea7ca-112">Задает миграцию пространства имен "NamespaceStandardMirgation" как завершенного.</span><span class="sxs-lookup"><span data-stu-id="ea7ca-112">Sets the Migration of 'NamespaceStandardMirgation' namespace as complete.</span></span>

## <span data-ttu-id="ea7ca-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ea7ca-113">PARAMETERS</span></span>

### <span data-ttu-id="ea7ca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea7ca-114">-DefaultProfile</span></span>
<span data-ttu-id="ea7ca-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ea7ca-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea7ca-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea7ca-116">-InputObject</span></span>
<span data-ttu-id="ea7ca-117">Настройка миграции служебной шины — стандартный объект пространства имен</span><span class="sxs-lookup"><span data-stu-id="ea7ca-117">Service Bus Migration configuration - Standard Namespace Object</span></span>

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

### <span data-ttu-id="ea7ca-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ea7ca-118">-Name</span></span>
<span data-ttu-id="ea7ca-119">Имя стандартного пространства имен</span><span class="sxs-lookup"><span data-stu-id="ea7ca-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="ea7ca-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ea7ca-120">-PassThru</span></span>
<span data-ttu-id="ea7ca-121">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="ea7ca-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="ea7ca-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea7ca-122">-ResourceGroupName</span></span>
<span data-ttu-id="ea7ca-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ea7ca-123">Resource Group Name</span></span>

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

### <span data-ttu-id="ea7ca-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea7ca-124">-ResourceId</span></span>
<span data-ttu-id="ea7ca-125">Migratio служебной шины — идентификатор ресурса стандартного пространства имен</span><span class="sxs-lookup"><span data-stu-id="ea7ca-125">Service Bus Migratio - Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="ea7ca-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea7ca-126">-Confirm</span></span>
<span data-ttu-id="ea7ca-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ea7ca-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea7ca-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea7ca-128">-WhatIf</span></span>
<span data-ttu-id="ea7ca-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ea7ca-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea7ca-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ea7ca-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea7ca-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea7ca-131">CommonParameters</span></span>
<span data-ttu-id="ea7ca-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ea7ca-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea7ca-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea7ca-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea7ca-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ea7ca-134">INPUTS</span></span>

### <span data-ttu-id="ea7ca-135">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="ea7ca-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>
<span data-ttu-id="ea7ca-136">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ea7ca-136">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="ea7ca-137">System. String</span><span class="sxs-lookup"><span data-stu-id="ea7ca-137">System.String</span></span>

## <span data-ttu-id="ea7ca-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea7ca-138">OUTPUTS</span></span>

### <span data-ttu-id="ea7ca-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ea7ca-139">System.Boolean</span></span>

## <span data-ttu-id="ea7ca-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="ea7ca-140">NOTES</span></span>

## <span data-ttu-id="ea7ca-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ea7ca-141">RELATED LINKS</span></span>
