---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteFilter.md
ms.openlocfilehash: 3f7e0a96212e9de87c90cffd059801084da471ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564223"
---
# <span data-ttu-id="d8e4c-101">Remove-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="d8e4c-101">Remove-AzureRmRouteFilter</span></span>

## <span data-ttu-id="d8e4c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d8e4c-102">SYNOPSIS</span></span>
<span data-ttu-id="d8e4c-103">{Заполнение кратких описаний}</span><span class="sxs-lookup"><span data-stu-id="d8e4c-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8e4c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d8e4c-104">SYNTAX</span></span>

```
Remove-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8e4c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8e4c-105">DESCRIPTION</span></span>
<span data-ttu-id="d8e4c-106">{Заполнение в описании}}</span><span class="sxs-lookup"><span data-stu-id="d8e4c-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="d8e4c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d8e4c-107">EXAMPLES</span></span>

### <span data-ttu-id="d8e4c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d8e4c-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="d8e4c-109">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="d8e4c-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="d8e4c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d8e4c-110">PARAMETERS</span></span>

### <span data-ttu-id="d8e4c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8e4c-111">-DefaultProfile</span></span>
<span data-ttu-id="d8e4c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d8e4c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8e4c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="d8e4c-113">-Force</span></span>
<span data-ttu-id="d8e4c-114">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="d8e4c-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d8e4c-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d8e4c-115">-Name</span></span>
<span data-ttu-id="d8e4c-116">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="d8e4c-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8e4c-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d8e4c-117">-PassThru</span></span>
<span data-ttu-id="d8e4c-118">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="d8e4c-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d8e4c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8e4c-119">-ResourceGroupName</span></span>
<span data-ttu-id="d8e4c-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d8e4c-120">The resource group name.</span></span>

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

### <span data-ttu-id="d8e4c-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8e4c-121">-Confirm</span></span>
<span data-ttu-id="d8e4c-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d8e4c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8e4c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8e4c-123">-WhatIf</span></span>
<span data-ttu-id="d8e4c-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d8e4c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8e4c-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d8e4c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8e4c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8e4c-126">CommonParameters</span></span>
<span data-ttu-id="d8e4c-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d8e4c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8e4c-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8e4c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8e4c-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d8e4c-129">INPUTS</span></span>

### <span data-ttu-id="d8e4c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d8e4c-130">System.String</span></span>

## <span data-ttu-id="d8e4c-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8e4c-131">OUTPUTS</span></span>

### <span data-ttu-id="d8e4c-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d8e4c-132">System.Boolean</span></span>

## <span data-ttu-id="d8e4c-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="d8e4c-133">NOTES</span></span>

## <span data-ttu-id="d8e4c-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d8e4c-134">RELATED LINKS</span></span>
