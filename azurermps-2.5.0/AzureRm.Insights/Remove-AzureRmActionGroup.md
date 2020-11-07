---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermactiongroup
schema: 2.0.0
ms.openlocfilehash: 7ec50b0698017c20fb47030ccb571d6b4083b97b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913888"
---
# <span data-ttu-id="acddc-101">Remove-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="acddc-101">Remove-AzureRmActionGroup</span></span>

## <span data-ttu-id="acddc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="acddc-102">SYNOPSIS</span></span>
<span data-ttu-id="acddc-103">Удаление группы действий.</span><span class="sxs-lookup"><span data-stu-id="acddc-103">Removes an action group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="acddc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="acddc-104">SYNTAX</span></span>

### <span data-ttu-id="acddc-105">ByPropertyName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="acddc-105">ByPropertyName (Default)</span></span>
```
Remove-AzureRmActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acddc-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="acddc-106">ByResourceId</span></span>
```
Remove-AzureRmActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="acddc-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="acddc-107">ByInputObject</span></span>
```
Remove-AzureRmActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acddc-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="acddc-108">DESCRIPTION</span></span>
<span data-ttu-id="acddc-109">Командлет **Remove-AzureRmActionGroup** удаляет группу действий.</span><span class="sxs-lookup"><span data-stu-id="acddc-109">The **Remove-AzureRmActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="acddc-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="acddc-110">EXAMPLES</span></span>

### <span data-ttu-id="acddc-111">Пример 1: Удаление группы действий</span><span class="sxs-lookup"><span data-stu-id="acddc-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzureRmActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="acddc-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="acddc-112">PARAMETERS</span></span>

### <span data-ttu-id="acddc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acddc-113">-DefaultProfile</span></span>
<span data-ttu-id="acddc-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="acddc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="acddc-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="acddc-115">-InputObject</span></span>
<span data-ttu-id="acddc-116">Группа "действия" resourc</span><span class="sxs-lookup"><span data-stu-id="acddc-116">The action group resourc</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="acddc-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="acddc-117">-Name</span></span>
<span data-ttu-id="acddc-118">Имя группы действий.</span><span class="sxs-lookup"><span data-stu-id="acddc-118">The name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acddc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acddc-119">-ResourceGroupName</span></span>
<span data-ttu-id="acddc-120">"Группа ресурсов"</span><span class="sxs-lookup"><span data-stu-id="acddc-120">The resource group nam</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acddc-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="acddc-121">-ResourceId</span></span>
<span data-ttu-id="acddc-122">Ресурс</span><span class="sxs-lookup"><span data-stu-id="acddc-122">The resource i</span></span>

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

### <span data-ttu-id="acddc-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="acddc-123">-Confirm</span></span>
<span data-ttu-id="acddc-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="acddc-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acddc-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acddc-125">-WhatIf</span></span>
<span data-ttu-id="acddc-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="acddc-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="acddc-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="acddc-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acddc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acddc-128">CommonParameters</span></span>
<span data-ttu-id="acddc-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="acddc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acddc-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acddc-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acddc-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="acddc-131">INPUTS</span></span>

### <span data-ttu-id="acddc-132">System. String</span><span class="sxs-lookup"><span data-stu-id="acddc-132">System.String</span></span>

### <span data-ttu-id="acddc-133">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="acddc-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>
<span data-ttu-id="acddc-134">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="acddc-134">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="acddc-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="acddc-135">OUTPUTS</span></span>

### <span data-ttu-id="acddc-136">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="acddc-136">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="acddc-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="acddc-137">NOTES</span></span>

## <span data-ttu-id="acddc-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="acddc-138">RELATED LINKS</span></span>

<span data-ttu-id="acddc-139">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="acddc-139">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
