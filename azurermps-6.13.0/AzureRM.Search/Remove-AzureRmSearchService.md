---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/remove-azurermsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Remove-AzureRmSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Remove-AzureRmSearchService.md
ms.openlocfilehash: c558a5d7228253e0a76b0d47fb21f581b4e06f11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566763"
---
# <span data-ttu-id="ed60f-101">Remove-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="ed60f-101">Remove-AzureRmSearchService</span></span>

## <span data-ttu-id="ed60f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ed60f-102">SYNOPSIS</span></span>
<span data-ttu-id="ed60f-103">Удалите службу поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="ed60f-103">Remove an Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed60f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ed60f-104">SYNTAX</span></span>

### <span data-ttu-id="ed60f-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ed60f-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzureRmSearchService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed60f-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed60f-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmSearchService [-InputObject] <PSSearchService> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed60f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed60f-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmSearchService [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed60f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed60f-108">DESCRIPTION</span></span>
<span data-ttu-id="ed60f-109">Командлет **Remove-AzureRmSearchService** Удаляет службу поиска Azure с указанным paramters.</span><span class="sxs-lookup"><span data-stu-id="ed60f-109">The **Remove-AzureRmSearchService** cmdlet removes an Azure Search service with specified paramters.</span></span>

## <span data-ttu-id="ed60f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ed60f-110">EXAMPLES</span></span>

### <span data-ttu-id="ed60f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ed60f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01"

Confirm
Are you sure you want to remove Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="ed60f-112">В примере удаляется служба поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="ed60f-112">The example removes an Azure Search service.</span></span>

## <span data-ttu-id="ed60f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ed60f-113">PARAMETERS</span></span>

### <span data-ttu-id="ed60f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed60f-114">-DefaultProfile</span></span>
<span data-ttu-id="ed60f-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ed60f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed60f-116">-Force</span><span class="sxs-lookup"><span data-stu-id="ed60f-116">-Force</span></span>
<span data-ttu-id="ed60f-117">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="ed60f-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ed60f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed60f-118">-InputObject</span></span>
<span data-ttu-id="ed60f-119">Объект ввода службы поиска.</span><span class="sxs-lookup"><span data-stu-id="ed60f-119">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed60f-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ed60f-120">-Name</span></span>
<span data-ttu-id="ed60f-121">Имя службы поиска.</span><span class="sxs-lookup"><span data-stu-id="ed60f-121">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed60f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ed60f-122">-PassThru</span></span>
<span data-ttu-id="ed60f-123">Этот командлет не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ed60f-123">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="ed60f-124">Если этот параметр указан, функция возвращает значение истина, если операция завершилась успешно.</span><span class="sxs-lookup"><span data-stu-id="ed60f-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="ed60f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed60f-125">-ResourceGroupName</span></span>
<span data-ttu-id="ed60f-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ed60f-126">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed60f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed60f-127">-ResourceId</span></span>
<span data-ttu-id="ed60f-128">Идентификатор ресурса службы поиска.</span><span class="sxs-lookup"><span data-stu-id="ed60f-128">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed60f-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed60f-129">-Confirm</span></span>
<span data-ttu-id="ed60f-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ed60f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed60f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed60f-131">-WhatIf</span></span>
<span data-ttu-id="ed60f-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ed60f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed60f-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ed60f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed60f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed60f-134">CommonParameters</span></span>
<span data-ttu-id="ed60f-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ed60f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed60f-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed60f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed60f-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ed60f-137">INPUTS</span></span>

### <span data-ttu-id="ed60f-138">Microsoft. Azure. Commands. Management. Search. Models. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="ed60f-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="ed60f-139">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ed60f-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="ed60f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ed60f-140">System.String</span></span>

## <span data-ttu-id="ed60f-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed60f-141">OUTPUTS</span></span>

### <span data-ttu-id="ed60f-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ed60f-142">System.Boolean</span></span>

## <span data-ttu-id="ed60f-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="ed60f-143">NOTES</span></span>

## <span data-ttu-id="ed60f-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ed60f-144">RELATED LINKS</span></span>

[<span data-ttu-id="ed60f-145">New-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="ed60f-145">New-AzureRmSearchService</span></span>](./New-AzureRmSearchService.md)

[<span data-ttu-id="ed60f-146">Get-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="ed60f-146">Get-AzureRmSearchService</span></span>](./Get-AzureRmSearchService.md)

[<span data-ttu-id="ed60f-147">Set-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="ed60f-147">Set-AzureRmSearchService</span></span>](./Set-AzureRmSearchService.md)

