---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzSecurityPartnerProvider.md
ms.openlocfilehash: a51345653580261178191687f54bf0f2a8cc6f0c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100236545"
---
# <span data-ttu-id="76f4d-101">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="76f4d-101">Remove-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="76f4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76f4d-102">SYNOPSIS</span></span>
<span data-ttu-id="76f4d-103">Удаляет Azure SecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="76f4d-103">Deletes an Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="76f4d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="76f4d-104">SYNTAX</span></span>

### <span data-ttu-id="76f4d-105">SecurityPartnerProviderNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="76f4d-105">SecurityPartnerProviderNameParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76f4d-106">SecurityPartnerProviderInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="76f4d-106">SecurityPartnerProviderInputObjectParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -SecurityPartnerProvider <PSSecurityPartnerProvider> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76f4d-107">SecurityPartnerProviderResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="76f4d-107">SecurityPartnerProviderResourceIdParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76f4d-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="76f4d-108">DESCRIPTION</span></span>
<span data-ttu-id="76f4d-109">**Cmdlet Remove-AzSecurityPartnerProvider** удаляет Azure SecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="76f4d-109">The **Remove-AzSecurityPartnerProvider** cmdlet deletes an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="76f4d-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="76f4d-110">EXAMPLES</span></span>

### <span data-ttu-id="76f4d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="76f4d-111">Example 1</span></span>
```powershell
Remove-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
```

## <span data-ttu-id="76f4d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76f4d-112">PARAMETERS</span></span>

### <span data-ttu-id="76f4d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76f4d-113">-AsJob</span></span>
<span data-ttu-id="76f4d-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="76f4d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="76f4d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76f4d-115">-DefaultProfile</span></span>
<span data-ttu-id="76f4d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="76f4d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76f4d-117">-Force</span><span class="sxs-lookup"><span data-stu-id="76f4d-117">-Force</span></span>
<span data-ttu-id="76f4d-118">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="76f4d-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="76f4d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="76f4d-119">-Name</span></span>
<span data-ttu-id="76f4d-120">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="76f4d-120">The resource name.</span></span>

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

### <span data-ttu-id="76f4d-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="76f4d-121">-PassThru</span></span>
<span data-ttu-id="76f4d-122">Возвращает объект, представляющий элемент, для которого выполняется эта операция.</span><span class="sxs-lookup"><span data-stu-id="76f4d-122">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="76f4d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76f4d-123">-ResourceGroupName</span></span>
<span data-ttu-id="76f4d-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="76f4d-124">The resource group name.</span></span>

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

### <span data-ttu-id="76f4d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76f4d-125">-ResourceId</span></span>
<span data-ttu-id="76f4d-126">ИД ресурса securityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="76f4d-126">The securityPartnerProvider resource Id.</span></span>

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

### <span data-ttu-id="76f4d-127">-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="76f4d-127">-SecurityPartnerProvider</span></span>
<span data-ttu-id="76f4d-128">Объект ввода securityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="76f4d-128">The securityPartnerProvider input object.</span></span>

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

### <span data-ttu-id="76f4d-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76f4d-129">-Confirm</span></span>
<span data-ttu-id="76f4d-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76f4d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76f4d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76f4d-131">-WhatIf</span></span>
<span data-ttu-id="76f4d-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76f4d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76f4d-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="76f4d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76f4d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76f4d-134">CommonParameters</span></span>
<span data-ttu-id="76f4d-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76f4d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76f4d-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76f4d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76f4d-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="76f4d-137">INPUTS</span></span>

### <span data-ttu-id="76f4d-138">System.String</span><span class="sxs-lookup"><span data-stu-id="76f4d-138">System.String</span></span>

### <span data-ttu-id="76f4d-139">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="76f4d-139">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="76f4d-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="76f4d-140">OUTPUTS</span></span>

### <span data-ttu-id="76f4d-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="76f4d-141">System.Boolean</span></span>

## <span data-ttu-id="76f4d-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="76f4d-142">NOTES</span></span>

## <span data-ttu-id="76f4d-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="76f4d-143">RELATED LINKS</span></span>
