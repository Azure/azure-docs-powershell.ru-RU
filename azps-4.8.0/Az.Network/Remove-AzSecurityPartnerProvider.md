---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzSecurityPartnerProvider.md
ms.openlocfilehash: a51345653580261178191687f54bf0f2a8cc6f0c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244081"
---
# <span data-ttu-id="c99b9-101">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="c99b9-101">Remove-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="c99b9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c99b9-102">SYNOPSIS</span></span>
<span data-ttu-id="c99b9-103">Удаление SecurityPartnerProvider Azure.</span><span class="sxs-lookup"><span data-stu-id="c99b9-103">Deletes an Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="c99b9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c99b9-104">SYNTAX</span></span>

### <span data-ttu-id="c99b9-105">SecurityPartnerProviderNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c99b9-105">SecurityPartnerProviderNameParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c99b9-106">SecurityPartnerProviderInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c99b9-106">SecurityPartnerProviderInputObjectParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -SecurityPartnerProvider <PSSecurityPartnerProvider> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c99b9-107">SecurityPartnerProviderResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c99b9-107">SecurityPartnerProviderResourceIdParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c99b9-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c99b9-108">DESCRIPTION</span></span>
<span data-ttu-id="c99b9-109">Командлет **Remove-AzSecurityPartnerProvider** удаляет Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="c99b9-109">The **Remove-AzSecurityPartnerProvider** cmdlet deletes an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="c99b9-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c99b9-110">EXAMPLES</span></span>

### <span data-ttu-id="c99b9-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c99b9-111">Example 1</span></span>
```powershell
Remove-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
```

## <span data-ttu-id="c99b9-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c99b9-112">PARAMETERS</span></span>

### <span data-ttu-id="c99b9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c99b9-113">-AsJob</span></span>
<span data-ttu-id="c99b9-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c99b9-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c99b9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c99b9-115">-DefaultProfile</span></span>
<span data-ttu-id="c99b9-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c99b9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c99b9-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c99b9-117">-Force</span></span>
<span data-ttu-id="c99b9-118">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="c99b9-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c99b9-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c99b9-119">-Name</span></span>
<span data-ttu-id="c99b9-120">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="c99b9-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c99b9-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c99b9-121">-PassThru</span></span>
<span data-ttu-id="c99b9-122">Возвращает объект, представляющий элемент, для которого выполняется операция.</span><span class="sxs-lookup"><span data-stu-id="c99b9-122">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="c99b9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c99b9-123">-ResourceGroupName</span></span>
<span data-ttu-id="c99b9-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c99b9-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c99b9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c99b9-125">-ResourceId</span></span>
<span data-ttu-id="c99b9-126">Идентификатор ресурса securityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="c99b9-126">The securityPartnerProvider resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c99b9-127">-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="c99b9-127">-SecurityPartnerProvider</span></span>
<span data-ttu-id="c99b9-128">Объект ввода securityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="c99b9-128">The securityPartnerProvider input object.</span></span>

```yaml
Type: PSSecurityPartnerProvider
Parameter Sets: SecurityPartnerProviderInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c99b9-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c99b9-129">-Confirm</span></span>
<span data-ttu-id="c99b9-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c99b9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c99b9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c99b9-131">-WhatIf</span></span>
<span data-ttu-id="c99b9-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c99b9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c99b9-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c99b9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c99b9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c99b9-134">CommonParameters</span></span>
<span data-ttu-id="c99b9-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c99b9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c99b9-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c99b9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c99b9-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c99b9-137">INPUTS</span></span>

### <span data-ttu-id="c99b9-138">System. String</span><span class="sxs-lookup"><span data-stu-id="c99b9-138">System.String</span></span>

### <span data-ttu-id="c99b9-139">Microsoft. Azure. Commands. Network. Models. PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="c99b9-139">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="c99b9-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c99b9-140">OUTPUTS</span></span>

### <span data-ttu-id="c99b9-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c99b9-141">System.Boolean</span></span>

## <span data-ttu-id="c99b9-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="c99b9-142">NOTES</span></span>

## <span data-ttu-id="c99b9-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c99b9-143">RELATED LINKS</span></span>
