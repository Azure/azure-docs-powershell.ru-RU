---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 00cfc136465cc250d068344158d66f98dc6e0704
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074568"
---
# <span data-ttu-id="e659a-101">Remove-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="e659a-101">Remove-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="e659a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e659a-102">SYNOPSIS</span></span>
<span data-ttu-id="e659a-103">Удаление учетных данных учетной записи хранения для устройства.</span><span class="sxs-lookup"><span data-stu-id="e659a-103">Removes a storage account credential for a device.</span></span>

## <span data-ttu-id="e659a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e659a-104">SYNTAX</span></span>

### <span data-ttu-id="e659a-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e659a-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e659a-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e659a-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccountCredential [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e659a-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e659a-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccountCredential [-InputObject] <PSDataBoxEdgeStorageAccountCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e659a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e659a-108">DESCRIPTION</span></span>
<span data-ttu-id="e659a-109">Командлет **Remove-AzDataBoxEdgeStorageAccountCredential** удаляет учетные данные учетной записи хранения на пограничном устройстве поля данных.</span><span class="sxs-lookup"><span data-stu-id="e659a-109">The **Remove-AzDataBoxEdgeStorageAccountCredential** cmdlet removes the storage account credential for a Data Box Edge device.</span></span>

## <span data-ttu-id="e659a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e659a-110">EXAMPLES</span></span>

### <span data-ttu-id="e659a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e659a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeStorageAccountCredential ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAccountCredentialName
```

## <span data-ttu-id="e659a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e659a-112">PARAMETERS</span></span>

### <span data-ttu-id="e659a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e659a-113">-AsJob</span></span>
<span data-ttu-id="e659a-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e659a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e659a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e659a-115">-DefaultProfile</span></span>
<span data-ttu-id="e659a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e659a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e659a-117">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="e659a-117">-DeviceName</span></span>
<span data-ttu-id="e659a-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="e659a-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e659a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e659a-119">-InputObject</span></span>
<span data-ttu-id="e659a-120">Объект input</span><span class="sxs-lookup"><span data-stu-id="e659a-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e659a-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e659a-121">-Name</span></span>
<span data-ttu-id="e659a-122">Имя учетной записи хранения, которую нужно использовать</span><span class="sxs-lookup"><span data-stu-id="e659a-122">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e659a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e659a-123">-PassThru</span></span>
<span data-ttu-id="e659a-124">Возвращает значение истина, если выполнено успешно</span><span class="sxs-lookup"><span data-stu-id="e659a-124">returns true if successful</span></span>

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

### <span data-ttu-id="e659a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e659a-125">-ResourceGroupName</span></span>
<span data-ttu-id="e659a-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="e659a-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e659a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e659a-127">-ResourceId</span></span>
<span data-ttu-id="e659a-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="e659a-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e659a-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e659a-129">-Confirm</span></span>
<span data-ttu-id="e659a-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e659a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e659a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e659a-131">-WhatIf</span></span>
<span data-ttu-id="e659a-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e659a-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e659a-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e659a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e659a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e659a-134">CommonParameters</span></span>
<span data-ttu-id="e659a-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e659a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e659a-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e659a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e659a-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e659a-137">INPUTS</span></span>

### <span data-ttu-id="e659a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e659a-138">System.String</span></span>

### <span data-ttu-id="e659a-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="e659a-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="e659a-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e659a-140">OUTPUTS</span></span>

### <span data-ttu-id="e659a-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e659a-141">System.Boolean</span></span>

## <span data-ttu-id="e659a-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="e659a-142">NOTES</span></span>

## <span data-ttu-id="e659a-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e659a-143">RELATED LINKS</span></span>
