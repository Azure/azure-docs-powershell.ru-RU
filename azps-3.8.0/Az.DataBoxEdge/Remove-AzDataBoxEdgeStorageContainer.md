---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: 0e952ba845398fcd221ca7e5f4177a103b1f6155
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074571"
---
# <span data-ttu-id="cb45c-101">Remove-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="cb45c-101">Remove-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="cb45c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cb45c-102">SYNOPSIS</span></span>
<span data-ttu-id="cb45c-103">Удаление контейнера хранилища для учетной записи хранилища EDGE на устройстве.</span><span class="sxs-lookup"><span data-stu-id="cb45c-103">Removes a storage container for the Edge Storage account on a device.</span></span>

## <span data-ttu-id="cb45c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cb45c-104">SYNTAX</span></span>

### <span data-ttu-id="cb45c-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cb45c-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb45c-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb45c-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageContainer -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb45c-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb45c-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageContainer -InputObject <PSDataBoxEdgeStorageContainer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb45c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb45c-108">DESCRIPTION</span></span>
<span data-ttu-id="cb45c-109">Командлет **Remove-AzDataBoxEdgeStorageContainer** удаляет связанный контейнер хранилища для учетной записи хранилища EDGE на пограничном устройстве поля данных.</span><span class="sxs-lookup"><span data-stu-id="cb45c-109">The **Remove-AzDataBoxEdgeStorageContainer** cmdlet removes an associated storage container for the Edge Storage account on a Data Box Edge device.</span></span> <span data-ttu-id="cb45c-110">Вы можете указать имя контейнера хранилища, который нужно удалить в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="cb45c-110">You can specify the name of the storage container to be removed as a parameter.</span></span>

## <span data-ttu-id="cb45c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cb45c-111">EXAMPLES</span></span>

### <span data-ttu-id="cb45c-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cb45c-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccountname -Name container1
```

## <span data-ttu-id="cb45c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cb45c-113">PARAMETERS</span></span>

### <span data-ttu-id="cb45c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb45c-114">-AsJob</span></span>
<span data-ttu-id="cb45c-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="cb45c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cb45c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb45c-116">-DefaultProfile</span></span>
<span data-ttu-id="cb45c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cb45c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb45c-118">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="cb45c-118">-DeviceName</span></span>
<span data-ttu-id="cb45c-119">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="cb45c-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb45c-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cb45c-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="cb45c-121">Укажите имя существующего EdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cb45c-121">Provide existing EdgeStorageAccount's Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb45c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb45c-122">-InputObject</span></span>
<span data-ttu-id="cb45c-123">Объект input</span><span class="sxs-lookup"><span data-stu-id="cb45c-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb45c-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cb45c-124">-Name</span></span>
<span data-ttu-id="cb45c-125">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="cb45c-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb45c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb45c-126">-PassThru</span></span>
<span data-ttu-id="cb45c-127">Возвращает значение истина, если выполнено успешно</span><span class="sxs-lookup"><span data-stu-id="cb45c-127">returns true if successful</span></span>

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

### <span data-ttu-id="cb45c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb45c-128">-ResourceGroupName</span></span>
<span data-ttu-id="cb45c-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="cb45c-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb45c-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb45c-130">-ResourceId</span></span>
<span data-ttu-id="cb45c-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb45c-131">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb45c-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cb45c-132">-Confirm</span></span>
<span data-ttu-id="cb45c-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cb45c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb45c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb45c-134">-WhatIf</span></span>
<span data-ttu-id="cb45c-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cb45c-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cb45c-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cb45c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb45c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb45c-137">CommonParameters</span></span>
<span data-ttu-id="cb45c-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cb45c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb45c-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cb45c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb45c-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cb45c-140">INPUTS</span></span>

### <span data-ttu-id="cb45c-141">System. String</span><span class="sxs-lookup"><span data-stu-id="cb45c-141">System.String</span></span>

### <span data-ttu-id="cb45c-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="cb45c-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="cb45c-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb45c-143">OUTPUTS</span></span>

### <span data-ttu-id="cb45c-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cb45c-144">System.Boolean</span></span>

## <span data-ttu-id="cb45c-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="cb45c-145">NOTES</span></span>

## <span data-ttu-id="cb45c-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cb45c-146">RELATED LINKS</span></span>
