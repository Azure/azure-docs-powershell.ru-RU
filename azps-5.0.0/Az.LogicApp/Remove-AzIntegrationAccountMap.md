---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7AAF2ACC-84ED-449C-B1E8-F074463F44EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountMap.md
ms.openlocfilehash: 37e6fcbaf1347d9aec48f680de749bf0b967551a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248963"
---
# <span data-ttu-id="38735-101">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="38735-101">Remove-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="38735-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="38735-102">SYNOPSIS</span></span>
<span data-ttu-id="38735-103">Удаляет карту учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="38735-103">Removes an integration account map.</span></span>

## <span data-ttu-id="38735-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="38735-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38735-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="38735-105">DESCRIPTION</span></span>
<span data-ttu-id="38735-106">Командлет **Remove-AzIntegrationAccountMap** удаляет карту учетной записи интеграции из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="38735-106">The **Remove-AzIntegrationAccountMap** cmdlet removes an integration account map from a resource group.</span></span>
<span data-ttu-id="38735-107">Укажите имя учетной записи интеграции, имя группы ресурсов и имя карты.</span><span class="sxs-lookup"><span data-stu-id="38735-107">Specify the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="38735-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="38735-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="38735-109">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="38735-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="38735-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="38735-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="38735-111">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="38735-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="38735-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="38735-112">EXAMPLES</span></span>

### <span data-ttu-id="38735-113">Пример 1: удаление карты учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="38735-113">Example 1: Remove an integration account map</span></span>
```
PS C:\>Remove-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
```

<span data-ttu-id="38735-114">Эта команда удаляет карту учетной записи интеграции с именем IntegrationAccountMap47.</span><span class="sxs-lookup"><span data-stu-id="38735-114">This command removes the integration account map named IntegrationAccountMap47.</span></span>

## <span data-ttu-id="38735-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="38735-115">PARAMETERS</span></span>

### <span data-ttu-id="38735-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38735-116">-DefaultProfile</span></span>
<span data-ttu-id="38735-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="38735-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38735-118">-Force</span><span class="sxs-lookup"><span data-stu-id="38735-118">-Force</span></span>
<span data-ttu-id="38735-119">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="38735-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="38735-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="38735-120">-MapName</span></span>
<span data-ttu-id="38735-121">Указывает имя карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="38735-121">Specifies the name of the integration account map.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38735-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="38735-122">-Name</span></span>
<span data-ttu-id="38735-123">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="38735-123">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38735-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38735-124">-ResourceGroupName</span></span>
<span data-ttu-id="38735-125">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="38735-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38735-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38735-126">-Confirm</span></span>
<span data-ttu-id="38735-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="38735-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38735-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38735-128">-WhatIf</span></span>
<span data-ttu-id="38735-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="38735-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38735-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="38735-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38735-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38735-131">CommonParameters</span></span>
<span data-ttu-id="38735-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="38735-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38735-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38735-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38735-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="38735-134">INPUTS</span></span>

### <span data-ttu-id="38735-135">System. String</span><span class="sxs-lookup"><span data-stu-id="38735-135">System.String</span></span>

## <span data-ttu-id="38735-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="38735-136">OUTPUTS</span></span>

### <span data-ttu-id="38735-137">System. void</span><span class="sxs-lookup"><span data-stu-id="38735-137">System.Void</span></span>

## <span data-ttu-id="38735-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="38735-138">NOTES</span></span>

## <span data-ttu-id="38735-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="38735-139">RELATED LINKS</span></span>

[<span data-ttu-id="38735-140">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="38735-140">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="38735-141">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="38735-141">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="38735-142">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="38735-142">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)

