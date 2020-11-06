---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmServiceEndpointPolicy.md
ms.openlocfilehash: f3871e23c0d193ef2ea89c43e3a30c5597abbfe0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568458"
---
# <span data-ttu-id="ef2be-101">Remove-AzureRmServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ef2be-101">Remove-AzureRmServiceEndpointPolicy</span></span>

## <span data-ttu-id="ef2be-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ef2be-102">SYNOPSIS</span></span>
<span data-ttu-id="ef2be-103">{Заполнение кратких описаний}</span><span class="sxs-lookup"><span data-stu-id="ef2be-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef2be-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ef2be-104">SYNTAX</span></span>

```
Remove-AzureRmServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef2be-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef2be-105">DESCRIPTION</span></span>
<span data-ttu-id="ef2be-106">Командлет **Remove-AzureRmServiceEndpointPolicy** удаляет политику конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="ef2be-106">The **Remove-AzureRmServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="ef2be-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ef2be-107">EXAMPLES</span></span>

### <span data-ttu-id="ef2be-108">Пример 1: Удаление политики конечной точки службы с помощью имени</span><span class="sxs-lookup"><span data-stu-id="ef2be-108">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzureRmServiceEndpointPolicy -Name "Policy1" -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="ef2be-109">Эта команда удаляет политику конечной точки службы с именем Policy1, которая принадлежит к параметру resourcegroup с именем "resourcegroup1".</span><span class="sxs-lookup"><span data-stu-id="ef2be-109">This command removes a service endpoint policy with name Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

### <span data-ttu-id="ef2be-110">Пример 2: Удаление политики конечной точки службы с помощью объекта input</span><span class="sxs-lookup"><span data-stu-id="ef2be-110">Example 2: Remove a service endpoint policy using input object</span></span>
```
Remove-AzureRmServiceEndpointPolicy -InputObject $Policy1 -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="ef2be-111">Эта команда удаляет объект политики конечной точки службы Policy1, который принадлежит к параметру resourcegroup с именем "resourcegroup1".</span><span class="sxs-lookup"><span data-stu-id="ef2be-111">This command removes a service endpoint policy object Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

## <span data-ttu-id="ef2be-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ef2be-112">PARAMETERS</span></span>

### <span data-ttu-id="ef2be-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef2be-113">-DefaultProfile</span></span>
<span data-ttu-id="ef2be-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ef2be-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef2be-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ef2be-115">-Force</span></span>
<span data-ttu-id="ef2be-116">Не запрашивать подтверждение, если вы хотите переделать ресурс</span><span class="sxs-lookup"><span data-stu-id="ef2be-116">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef2be-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ef2be-117">-Name</span></span>
<span data-ttu-id="ef2be-118">Имя политики конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="ef2be-118">The name of the service endpoint policy</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef2be-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef2be-119">-PassThru</span></span>
<span data-ttu-id="ef2be-120">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="ef2be-120">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef2be-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef2be-121">-ResourceGroupName</span></span>
<span data-ttu-id="ef2be-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ef2be-122">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef2be-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef2be-123">-Confirm</span></span>
<span data-ttu-id="ef2be-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ef2be-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef2be-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef2be-125">-WhatIf</span></span>
<span data-ttu-id="ef2be-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ef2be-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef2be-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ef2be-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef2be-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef2be-128">CommonParameters</span></span>
<span data-ttu-id="ef2be-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ef2be-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ef2be-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef2be-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef2be-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ef2be-131">INPUTS</span></span>

### <span data-ttu-id="ef2be-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ef2be-132">System.String</span></span>


## <span data-ttu-id="ef2be-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef2be-133">OUTPUTS</span></span>

### <span data-ttu-id="ef2be-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="ef2be-134">System.Object</span></span>

## <span data-ttu-id="ef2be-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="ef2be-135">NOTES</span></span>

## <span data-ttu-id="ef2be-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ef2be-136">RELATED LINKS</span></span>
