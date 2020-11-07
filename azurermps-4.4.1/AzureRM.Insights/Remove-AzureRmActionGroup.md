---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActionGroup.md
ms.openlocfilehash: 0b5f84a38fcd087b77b32624b9cbd9b3b8a27e05
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734557"
---
# <span data-ttu-id="a2c7f-101">Remove-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="a2c7f-101">Remove-AzureRmActionGroup</span></span>

## <span data-ttu-id="a2c7f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a2c7f-102">SYNOPSIS</span></span>
<span data-ttu-id="a2c7f-103">Удаление группы действий.</span><span class="sxs-lookup"><span data-stu-id="a2c7f-103">Removes an action group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2c7f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a2c7f-104">SYNTAX</span></span>

### <span data-ttu-id="a2c7f-105">ByPropertyName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a2c7f-105">ByPropertyName (Default)</span></span>
```
Remove-AzureRmActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2c7f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a2c7f-106">ByResourceId</span></span>
```
Remove-AzureRmActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a2c7f-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a2c7f-107">ByInputObject</span></span>
```
Remove-AzureRmActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2c7f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2c7f-108">DESCRIPTION</span></span>
<span data-ttu-id="a2c7f-109">Командлет **Remove-AzureRmActionGroup** удаляет группу действий.</span><span class="sxs-lookup"><span data-stu-id="a2c7f-109">The **Remove-AzureRmActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="a2c7f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a2c7f-110">EXAMPLES</span></span>

### <span data-ttu-id="a2c7f-111">Пример 1: Удаление группы действий</span><span class="sxs-lookup"><span data-stu-id="a2c7f-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzureRmActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="a2c7f-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a2c7f-112">PARAMETERS</span></span>

### <span data-ttu-id="a2c7f-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a2c7f-113">-Name</span></span>
<span data-ttu-id="a2c7f-114">Имя группы действий.</span><span class="sxs-lookup"><span data-stu-id="a2c7f-114">The name of the action group.</span></span>

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

### <span data-ttu-id="a2c7f-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2c7f-115">-Confirm</span></span>
<span data-ttu-id="a2c7f-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a2c7f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2c7f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2c7f-117">-DefaultProfile</span></span>
<span data-ttu-id="a2c7f-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a2c7f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2c7f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2c7f-119">-InputObject</span></span>
<span data-ttu-id="a2c7f-120">Ресурс группы действий</span><span class="sxs-lookup"><span data-stu-id="a2c7f-120">The action group resource</span></span>

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

### <span data-ttu-id="a2c7f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2c7f-121">-ResourceGroupName</span></span>
<span data-ttu-id="a2c7f-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a2c7f-122">The resource group name</span></span>

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

### <span data-ttu-id="a2c7f-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2c7f-123">-ResourceId</span></span>
<span data-ttu-id="a2c7f-124">Идентификатор ресурса</span><span class="sxs-lookup"><span data-stu-id="a2c7f-124">The resource id</span></span>

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

### <span data-ttu-id="a2c7f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2c7f-125">-WhatIf</span></span>
<span data-ttu-id="a2c7f-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a2c7f-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a2c7f-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a2c7f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2c7f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2c7f-128">CommonParameters</span></span>
<span data-ttu-id="a2c7f-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a2c7f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2c7f-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2c7f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2c7f-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a2c7f-131">INPUTS</span></span>

## <span data-ttu-id="a2c7f-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2c7f-132">OUTPUTS</span></span>

### <span data-ttu-id="a2c7f-133">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a2c7f-133">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="a2c7f-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="a2c7f-134">NOTES</span></span>

## <span data-ttu-id="a2c7f-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a2c7f-135">RELATED LINKS</span></span>

<span data-ttu-id="a2c7f-136">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="a2c7f-136">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
