---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 848ce0e0c5608271f1f8facb955aad2df95b6a0a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236288"
---
# <span data-ttu-id="e2f1e-101">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2f1e-101">Remove-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="e2f1e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e2f1e-102">SYNOPSIS</span></span>
<span data-ttu-id="e2f1e-103">Удаляет пакетную конфигурацию учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e2f1e-103">Removes an integration account batch configuration.</span></span>

## <span data-ttu-id="e2f1e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e2f1e-104">SYNTAX</span></span>

### <span data-ttu-id="e2f1e-105">ByIntegrationAccount (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e2f1e-105">ByIntegrationAccount (Default)</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2f1e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e2f1e-106">ByInputObject</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2f1e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e2f1e-107">ByResourceId</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2f1e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2f1e-108">DESCRIPTION</span></span>
<span data-ttu-id="e2f1e-109">Командлет **Remove-AzIntegrationAccountBatchConfiguration** удаляет пакетную конфигурацию из учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e2f1e-109">The **Remove-AzIntegrationAccountBatchConfiguration** cmdlet removes a batch configuration from an integration account.</span></span>

## <span data-ttu-id="e2f1e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e2f1e-110">EXAMPLES</span></span>

### <span data-ttu-id="e2f1e-111">Пример 1: Удаление конфигурации пакета с помощью параметров</span><span class="sxs-lookup"><span data-stu-id="e2f1e-111">Example 1: Remove a batch configuration by parameters</span></span>
```powershell
PS C:\> Remove-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig"
```

<span data-ttu-id="e2f1e-112">Удаляет пакетную конфигурацию с именем "sampleBatchConfig", расположенную в учетной записи интеграции "sampleIntegrationAccount".</span><span class="sxs-lookup"><span data-stu-id="e2f1e-112">Removes the batch configuration named "sampleBatchConfig" located in the integration account "sampleIntegrationAccount".</span></span>

## <span data-ttu-id="e2f1e-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e2f1e-113">PARAMETERS</span></span>

### <span data-ttu-id="e2f1e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2f1e-114">-DefaultProfile</span></span>
<span data-ttu-id="e2f1e-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e2f1e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2f1e-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2f1e-116">-InputObject</span></span>
<span data-ttu-id="e2f1e-117">Настройка пакетной учетной записи для интеграции.</span><span class="sxs-lookup"><span data-stu-id="e2f1e-117">An integration account batch configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2f1e-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e2f1e-118">-Name</span></span>
<span data-ttu-id="e2f1e-119">Название пакетной конфигурации учетной записи для интеграции.</span><span class="sxs-lookup"><span data-stu-id="e2f1e-119">The integration account batch configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: BatchConfigurationName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2f1e-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="e2f1e-120">-ParentName</span></span>
<span data-ttu-id="e2f1e-121">Имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e2f1e-121">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2f1e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2f1e-122">-PassThru</span></span>
<span data-ttu-id="e2f1e-123">Возвращает значение, указывающее, была ли команда успешной.</span><span class="sxs-lookup"><span data-stu-id="e2f1e-123">Return whether the command was successful or not.</span></span>

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

### <span data-ttu-id="e2f1e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2f1e-124">-ResourceGroupName</span></span>
<span data-ttu-id="e2f1e-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e2f1e-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2f1e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2f1e-126">-ResourceId</span></span>
<span data-ttu-id="e2f1e-127">Код ресурса конфигурации для пакетной службы учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e2f1e-127">The integration account batch configuration resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2f1e-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2f1e-128">-Confirm</span></span>
<span data-ttu-id="e2f1e-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e2f1e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2f1e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2f1e-130">-WhatIf</span></span>
<span data-ttu-id="e2f1e-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e2f1e-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e2f1e-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e2f1e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2f1e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2f1e-133">CommonParameters</span></span>
<span data-ttu-id="e2f1e-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e2f1e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2f1e-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2f1e-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2f1e-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e2f1e-136">INPUTS</span></span>

### <span data-ttu-id="e2f1e-137">Microsoft. Azure. Commands. LogicApp. Models. PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2f1e-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

### <span data-ttu-id="e2f1e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e2f1e-138">System.String</span></span>

## <span data-ttu-id="e2f1e-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2f1e-139">OUTPUTS</span></span>

### <span data-ttu-id="e2f1e-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e2f1e-140">System.Boolean</span></span>

## <span data-ttu-id="e2f1e-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="e2f1e-141">NOTES</span></span>

## <span data-ttu-id="e2f1e-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e2f1e-142">RELATED LINKS</span></span>
