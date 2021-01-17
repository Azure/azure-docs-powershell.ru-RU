---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 848ce0e0c5608271f1f8facb955aad2df95b6a0a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327266"
---
# <span data-ttu-id="78faf-101">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="78faf-101">Remove-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="78faf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78faf-102">SYNOPSIS</span></span>
<span data-ttu-id="78faf-103">Удаляет пакетную конфигурацию учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="78faf-103">Removes an integration account batch configuration.</span></span>

## <span data-ttu-id="78faf-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="78faf-104">SYNTAX</span></span>

### <span data-ttu-id="78faf-105">ByIntegrationAccount (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="78faf-105">ByIntegrationAccount (Default)</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78faf-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="78faf-106">ByInputObject</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78faf-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="78faf-107">ByResourceId</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78faf-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="78faf-108">DESCRIPTION</span></span>
<span data-ttu-id="78faf-109">Для удаления из учетной записи интеграции удаляется пакетная конфигурация **Remove-AzIntegrationAccountBatchConfiguration.**</span><span class="sxs-lookup"><span data-stu-id="78faf-109">The **Remove-AzIntegrationAccountBatchConfiguration** cmdlet removes a batch configuration from an integration account.</span></span>

## <span data-ttu-id="78faf-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="78faf-110">EXAMPLES</span></span>

### <span data-ttu-id="78faf-111">Пример 1. Удаление пакетной конфигурации по параметрам</span><span class="sxs-lookup"><span data-stu-id="78faf-111">Example 1: Remove a batch configuration by parameters</span></span>
```powershell
PS C:\> Remove-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig"
```

<span data-ttu-id="78faf-112">Удаляет пакетную конфигурацию sampleBatchConfig, расположенную в учетной записи интеграции sampleIntegrationAccount.</span><span class="sxs-lookup"><span data-stu-id="78faf-112">Removes the batch configuration named "sampleBatchConfig" located in the integration account "sampleIntegrationAccount".</span></span>

## <span data-ttu-id="78faf-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78faf-113">PARAMETERS</span></span>

### <span data-ttu-id="78faf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78faf-114">-DefaultProfile</span></span>
<span data-ttu-id="78faf-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="78faf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78faf-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78faf-116">-InputObject</span></span>
<span data-ttu-id="78faf-117">Пакетная конфигурация учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="78faf-117">An integration account batch configuration.</span></span>

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

### <span data-ttu-id="78faf-118">-Name</span><span class="sxs-lookup"><span data-stu-id="78faf-118">-Name</span></span>
<span data-ttu-id="78faf-119">Имя пакета конфигурации учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="78faf-119">The integration account batch configuration name.</span></span>

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

### <span data-ttu-id="78faf-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="78faf-120">-ParentName</span></span>
<span data-ttu-id="78faf-121">Имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="78faf-121">The integration account name.</span></span>

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

### <span data-ttu-id="78faf-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78faf-122">-PassThru</span></span>
<span data-ttu-id="78faf-123">Возвращает, была ли команда успешной.</span><span class="sxs-lookup"><span data-stu-id="78faf-123">Return whether the command was successful or not.</span></span>

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

### <span data-ttu-id="78faf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78faf-124">-ResourceGroupName</span></span>
<span data-ttu-id="78faf-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="78faf-125">The resource group name.</span></span>

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

### <span data-ttu-id="78faf-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78faf-126">-ResourceId</span></span>
<span data-ttu-id="78faf-127">ИД пакета конфигурации учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="78faf-127">The integration account batch configuration resource id.</span></span>

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

### <span data-ttu-id="78faf-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="78faf-128">-Confirm</span></span>
<span data-ttu-id="78faf-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="78faf-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78faf-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78faf-130">-WhatIf</span></span>
<span data-ttu-id="78faf-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78faf-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="78faf-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="78faf-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78faf-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78faf-133">CommonParameters</span></span>
<span data-ttu-id="78faf-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78faf-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78faf-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78faf-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78faf-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="78faf-136">INPUTS</span></span>

### <span data-ttu-id="78faf-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="78faf-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

### <span data-ttu-id="78faf-138">System.String</span><span class="sxs-lookup"><span data-stu-id="78faf-138">System.String</span></span>

## <span data-ttu-id="78faf-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="78faf-139">OUTPUTS</span></span>

### <span data-ttu-id="78faf-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="78faf-140">System.Boolean</span></span>

## <span data-ttu-id="78faf-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="78faf-141">NOTES</span></span>

## <span data-ttu-id="78faf-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="78faf-142">RELATED LINKS</span></span>
