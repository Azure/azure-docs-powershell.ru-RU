---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzSecurityPartnerProvider.md
ms.openlocfilehash: a51345653580261178191687f54bf0f2a8cc6f0c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408708"
---
# <span data-ttu-id="1a65b-101">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="1a65b-101">Remove-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="1a65b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a65b-102">SYNOPSIS</span></span>
<span data-ttu-id="1a65b-103">Удаляет Azure SecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="1a65b-103">Deletes an Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="1a65b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1a65b-104">SYNTAX</span></span>

### <span data-ttu-id="1a65b-105">SecurityPartnerProviderNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a65b-105">SecurityPartnerProviderNameParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a65b-106">SecurityPartnerProviderInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a65b-106">SecurityPartnerProviderInputObjectParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -SecurityPartnerProvider <PSSecurityPartnerProvider> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a65b-107">SecurityPartnerProviderResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a65b-107">SecurityPartnerProviderResourceIdParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a65b-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a65b-108">DESCRIPTION</span></span>
<span data-ttu-id="1a65b-109">**Cmdlet Remove-AzSecurityPartnerProvider** удаляет Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="1a65b-109">The **Remove-AzSecurityPartnerProvider** cmdlet deletes an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="1a65b-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1a65b-110">EXAMPLES</span></span>

### <span data-ttu-id="1a65b-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1a65b-111">Example 1</span></span>
```powershell
Remove-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
```

## <span data-ttu-id="1a65b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a65b-112">PARAMETERS</span></span>

### <span data-ttu-id="1a65b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a65b-113">-AsJob</span></span>
<span data-ttu-id="1a65b-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="1a65b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1a65b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a65b-115">-DefaultProfile</span></span>
<span data-ttu-id="1a65b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1a65b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a65b-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1a65b-117">-Force</span></span>
<span data-ttu-id="1a65b-118">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="1a65b-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1a65b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1a65b-119">-Name</span></span>
<span data-ttu-id="1a65b-120">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="1a65b-120">The resource name.</span></span>

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

### <span data-ttu-id="1a65b-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1a65b-121">-PassThru</span></span>
<span data-ttu-id="1a65b-122">Возвращает объект, представляющий элемент, с которым выполняется данной операция.</span><span class="sxs-lookup"><span data-stu-id="1a65b-122">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="1a65b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a65b-123">-ResourceGroupName</span></span>
<span data-ttu-id="1a65b-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1a65b-124">The resource group name.</span></span>

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

### <span data-ttu-id="1a65b-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a65b-125">-ResourceId</span></span>
<span data-ttu-id="1a65b-126">ИД ресурса securityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="1a65b-126">The securityPartnerProvider resource Id.</span></span>

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

### <span data-ttu-id="1a65b-127">-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="1a65b-127">-SecurityPartnerProvider</span></span>
<span data-ttu-id="1a65b-128">Объект ввода securityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="1a65b-128">The securityPartnerProvider input object.</span></span>

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

### <span data-ttu-id="1a65b-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1a65b-129">-Confirm</span></span>
<span data-ttu-id="1a65b-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a65b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a65b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a65b-131">-WhatIf</span></span>
<span data-ttu-id="1a65b-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a65b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a65b-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1a65b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a65b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a65b-134">CommonParameters</span></span>
<span data-ttu-id="1a65b-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a65b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a65b-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1a65b-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a65b-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1a65b-137">INPUTS</span></span>

### <span data-ttu-id="1a65b-138">System.String</span><span class="sxs-lookup"><span data-stu-id="1a65b-138">System.String</span></span>

### <span data-ttu-id="1a65b-139">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="1a65b-139">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="1a65b-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1a65b-140">OUTPUTS</span></span>

### <span data-ttu-id="1a65b-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1a65b-141">System.Boolean</span></span>

## <span data-ttu-id="1a65b-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1a65b-142">NOTES</span></span>

## <span data-ttu-id="1a65b-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1a65b-143">RELATED LINKS</span></span>
