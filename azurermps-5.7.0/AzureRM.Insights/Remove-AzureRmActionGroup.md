---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActionGroup.md
ms.openlocfilehash: 1d4a5365ac2112364a544eb2481a3193f23519c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566999"
---
# <span data-ttu-id="aad00-101">Remove-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="aad00-101">Remove-AzureRmActionGroup</span></span>

## <span data-ttu-id="aad00-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aad00-102">SYNOPSIS</span></span>
<span data-ttu-id="aad00-103">Удаление группы действий.</span><span class="sxs-lookup"><span data-stu-id="aad00-103">Removes an action group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aad00-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aad00-104">SYNTAX</span></span>

### <span data-ttu-id="aad00-105">ByPropertyName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="aad00-105">ByPropertyName (Default)</span></span>
```
Remove-AzureRmActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aad00-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="aad00-106">ByResourceId</span></span>
```
Remove-AzureRmActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aad00-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="aad00-107">ByInputObject</span></span>
```
Remove-AzureRmActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aad00-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aad00-108">DESCRIPTION</span></span>
<span data-ttu-id="aad00-109">Командлет **Remove-AzureRmActionGroup** удаляет группу действий.</span><span class="sxs-lookup"><span data-stu-id="aad00-109">The **Remove-AzureRmActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="aad00-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aad00-110">EXAMPLES</span></span>

### <span data-ttu-id="aad00-111">Пример 1: Удаление группы действий</span><span class="sxs-lookup"><span data-stu-id="aad00-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzureRmActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="aad00-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aad00-112">PARAMETERS</span></span>

### <span data-ttu-id="aad00-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aad00-113">-DefaultProfile</span></span>
<span data-ttu-id="aad00-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="aad00-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad00-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aad00-115">-InputObject</span></span>
<span data-ttu-id="aad00-116">Группа "действия" resourc</span><span class="sxs-lookup"><span data-stu-id="aad00-116">The action group resourc</span></span>

```yaml
Type: PSActionGroupResource
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aad00-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="aad00-117">-Name</span></span>
<span data-ttu-id="aad00-118">Имя группы действий.</span><span class="sxs-lookup"><span data-stu-id="aad00-118">The name of the action group.</span></span>

```yaml
Type: String
Parameter Sets: ByPropertyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aad00-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aad00-119">-ResourceGroupName</span></span>
<span data-ttu-id="aad00-120">"Группа ресурсов"</span><span class="sxs-lookup"><span data-stu-id="aad00-120">The resource group nam</span></span>

```yaml
Type: String
Parameter Sets: ByPropertyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aad00-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aad00-121">-ResourceId</span></span>
<span data-ttu-id="aad00-122">Ресурс</span><span class="sxs-lookup"><span data-stu-id="aad00-122">The resource i</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aad00-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aad00-123">-Confirm</span></span>
<span data-ttu-id="aad00-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="aad00-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad00-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aad00-125">-WhatIf</span></span>
<span data-ttu-id="aad00-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="aad00-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aad00-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="aad00-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aad00-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aad00-128">CommonParameters</span></span>
<span data-ttu-id="aad00-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aad00-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aad00-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aad00-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aad00-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aad00-131">INPUTS</span></span>

### <span data-ttu-id="aad00-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="aad00-132">None</span></span>
<span data-ttu-id="aad00-133">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="aad00-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="aad00-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aad00-134">OUTPUTS</span></span>

### <span data-ttu-id="aad00-135">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="aad00-135">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="aad00-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="aad00-136">NOTES</span></span>

## <span data-ttu-id="aad00-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aad00-137">RELATED LINKS</span></span>

<span data-ttu-id="aad00-138">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="aad00-138">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
