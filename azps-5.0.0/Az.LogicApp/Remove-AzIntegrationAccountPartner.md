---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: E8A557EA-FE3F-4433-BFDE-B4D73DF8467C
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountPartner.md
ms.openlocfilehash: ee4f24356c33aac0940a10905b52199bd06d2a47
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248959"
---
# <span data-ttu-id="f1cf8-101">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="f1cf8-101">Remove-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="f1cf8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f1cf8-102">SYNOPSIS</span></span>
<span data-ttu-id="f1cf8-103">Удаление партнера учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f1cf8-103">Removes an integration account partner.</span></span>

## <span data-ttu-id="f1cf8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f1cf8-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1cf8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1cf8-105">DESCRIPTION</span></span>
<span data-ttu-id="f1cf8-106">Командлет **Remove-AzIntegrationAccountPartner** удаляет партнера учетной записи интеграции из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f1cf8-106">The **Remove-AzIntegrationAccountPartner** cmdlet removes an integration account partner from a resource group.</span></span>
<span data-ttu-id="f1cf8-107">Укажите имя учетной записи интеграции, имя группы ресурсов и имя партнера.</span><span class="sxs-lookup"><span data-stu-id="f1cf8-107">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="f1cf8-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="f1cf8-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="f1cf8-109">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="f1cf8-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="f1cf8-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="f1cf8-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="f1cf8-111">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="f1cf8-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="f1cf8-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f1cf8-112">EXAMPLES</span></span>

### <span data-ttu-id="f1cf8-113">Пример 1: Удаление партнера учетной записи для интеграции</span><span class="sxs-lookup"><span data-stu-id="f1cf8-113">Example 1: Remove an integration account partner</span></span>
```
PS C:\>Remove-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner1"
```

<span data-ttu-id="f1cf8-114">Эта команда удаляет партнера учетной записи интеграции с именем IntegrationAccountPartner1.</span><span class="sxs-lookup"><span data-stu-id="f1cf8-114">This command removes the integration account partner named IntegrationAccountPartner1.</span></span>

## <span data-ttu-id="f1cf8-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f1cf8-115">PARAMETERS</span></span>

### <span data-ttu-id="f1cf8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1cf8-116">-DefaultProfile</span></span>
<span data-ttu-id="f1cf8-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f1cf8-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f1cf8-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f1cf8-118">-Force</span></span>
<span data-ttu-id="f1cf8-119">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="f1cf8-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f1cf8-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f1cf8-120">-Name</span></span>
<span data-ttu-id="f1cf8-121">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f1cf8-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="f1cf8-122">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="f1cf8-122">-PartnerName</span></span>
<span data-ttu-id="f1cf8-123">Указывает имя партнера учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f1cf8-123">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="f1cf8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1cf8-124">-ResourceGroupName</span></span>
<span data-ttu-id="f1cf8-125">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f1cf8-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f1cf8-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1cf8-126">-Confirm</span></span>
<span data-ttu-id="f1cf8-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f1cf8-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1cf8-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1cf8-128">-WhatIf</span></span>
<span data-ttu-id="f1cf8-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f1cf8-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1cf8-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f1cf8-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1cf8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1cf8-131">CommonParameters</span></span>
<span data-ttu-id="f1cf8-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f1cf8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1cf8-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1cf8-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1cf8-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f1cf8-134">INPUTS</span></span>

### <span data-ttu-id="f1cf8-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f1cf8-135">System.String</span></span>

## <span data-ttu-id="f1cf8-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1cf8-136">OUTPUTS</span></span>

### <span data-ttu-id="f1cf8-137">System. void</span><span class="sxs-lookup"><span data-stu-id="f1cf8-137">System.Void</span></span>

## <span data-ttu-id="f1cf8-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="f1cf8-138">NOTES</span></span>

## <span data-ttu-id="f1cf8-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f1cf8-139">RELATED LINKS</span></span>

[<span data-ttu-id="f1cf8-140">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="f1cf8-140">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="f1cf8-141">New-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="f1cf8-141">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="f1cf8-142">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="f1cf8-142">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)


