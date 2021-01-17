---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: E8A557EA-FE3F-4433-BFDE-B4D73DF8467C
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountPartner.md
ms.openlocfilehash: ee4f24356c33aac0940a10905b52199bd06d2a47
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401767"
---
# <span data-ttu-id="a1091-101">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="a1091-101">Remove-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="a1091-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1091-102">SYNOPSIS</span></span>
<span data-ttu-id="a1091-103">Удаляет партнера по интеграции с учетной записью.</span><span class="sxs-lookup"><span data-stu-id="a1091-103">Removes an integration account partner.</span></span>

## <span data-ttu-id="a1091-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a1091-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1091-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1091-105">DESCRIPTION</span></span>
<span data-ttu-id="a1091-106">Для **удаления из группы ресурсов** удаляется партнер учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="a1091-106">The **Remove-AzIntegrationAccountPartner** cmdlet removes an integration account partner from a resource group.</span></span>
<span data-ttu-id="a1091-107">Укажите имя учетной записи интеграции, имя группы ресурсов и имя партнера.</span><span class="sxs-lookup"><span data-stu-id="a1091-107">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="a1091-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="a1091-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="a1091-109">Чтобы использовать динамический параметр, введите его в команду.</span><span class="sxs-lookup"><span data-stu-id="a1091-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="a1091-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени cmdlet, а затем нажимая клавишу TAB для циклическиго перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="a1091-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a1091-111">Если параметр обязательного шаблона не задан, будет выдан запрос на его значение.</span><span class="sxs-lookup"><span data-stu-id="a1091-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a1091-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a1091-112">EXAMPLES</span></span>

### <span data-ttu-id="a1091-113">Пример 1. Удаление партнера учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="a1091-113">Example 1: Remove an integration account partner</span></span>
```
PS C:\>Remove-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner1"
```

<span data-ttu-id="a1091-114">Эта команда удаляет партнера по учетной записи интеграции IntegrationAccountPartner1.</span><span class="sxs-lookup"><span data-stu-id="a1091-114">This command removes the integration account partner named IntegrationAccountPartner1.</span></span>

## <span data-ttu-id="a1091-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1091-115">PARAMETERS</span></span>

### <span data-ttu-id="a1091-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1091-116">-DefaultProfile</span></span>
<span data-ttu-id="a1091-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a1091-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a1091-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a1091-118">-Force</span></span>
<span data-ttu-id="a1091-119">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="a1091-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a1091-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a1091-120">-Name</span></span>
<span data-ttu-id="a1091-121">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="a1091-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="a1091-122">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="a1091-122">-PartnerName</span></span>
<span data-ttu-id="a1091-123">Указывает имя партнера по учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="a1091-123">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="a1091-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1091-124">-ResourceGroupName</span></span>
<span data-ttu-id="a1091-125">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a1091-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a1091-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a1091-126">-Confirm</span></span>
<span data-ttu-id="a1091-127">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="a1091-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1091-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1091-128">-WhatIf</span></span>
<span data-ttu-id="a1091-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1091-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1091-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a1091-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1091-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1091-131">CommonParameters</span></span>
<span data-ttu-id="a1091-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1091-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1091-133">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1091-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1091-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a1091-134">INPUTS</span></span>

### <span data-ttu-id="a1091-135">System.String</span><span class="sxs-lookup"><span data-stu-id="a1091-135">System.String</span></span>

## <span data-ttu-id="a1091-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a1091-136">OUTPUTS</span></span>

### <span data-ttu-id="a1091-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="a1091-137">System.Void</span></span>

## <span data-ttu-id="a1091-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a1091-138">NOTES</span></span>

## <span data-ttu-id="a1091-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a1091-139">RELATED LINKS</span></span>

[<span data-ttu-id="a1091-140">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="a1091-140">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="a1091-141">New-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="a1091-141">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="a1091-142">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="a1091-142">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)


