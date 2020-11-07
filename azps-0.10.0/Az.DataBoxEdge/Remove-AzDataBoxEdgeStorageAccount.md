---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccount.md
ms.openlocfilehash: 4d69d14d1129deb1bff580a0e0edfdb922b1544d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911247"
---
# <span data-ttu-id="73f63-101">Remove-AzDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="73f63-101">Remove-AzDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="73f63-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="73f63-102">SYNOPSIS</span></span>
<span data-ttu-id="73f63-103">Удаление учетной записи хранилища Edge для устройства.</span><span class="sxs-lookup"><span data-stu-id="73f63-103">Removes the Edge Storage account for a device.</span></span>

## <span data-ttu-id="73f63-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="73f63-104">SYNTAX</span></span>

### <span data-ttu-id="73f63-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="73f63-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73f63-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="73f63-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73f63-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="73f63-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-InputObject] <PSDataBoxEdgeStorageAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73f63-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="73f63-108">DESCRIPTION</span></span>
<span data-ttu-id="73f63-109">Командлет **Remove-AzDataBoxEdgeStorageAccount** Удаляет связанную учетную запись хранилища пограничного устройства для поля данных.</span><span class="sxs-lookup"><span data-stu-id="73f63-109">The **Remove-AzDataBoxEdgeStorageAccount** cmdlet removes an associated Edge Storage Account for a Data Box Edge device.</span></span> <span data-ttu-id="73f63-110">Вы можете указать имя учетной записи хранения EDGE, которую нужно удалить как параметр в командлете.</span><span class="sxs-lookup"><span data-stu-id="73f63-110">You can specify the name of the Edge Storage Account to be removed as a parameter in the cmdlet.</span></span>

## <span data-ttu-id="73f63-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="73f63-111">EXAMPLES</span></span>

### <span data-ttu-id="73f63-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="73f63-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName deviceName -Name edgestorageaccountname
```

## <span data-ttu-id="73f63-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="73f63-113">PARAMETERS</span></span>

### <span data-ttu-id="73f63-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="73f63-114">-AsJob</span></span>
<span data-ttu-id="73f63-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="73f63-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="73f63-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73f63-116">-DefaultProfile</span></span>
<span data-ttu-id="73f63-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="73f63-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73f63-118">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="73f63-118">-DeviceName</span></span>
<span data-ttu-id="73f63-119">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="73f63-119">Device Name</span></span>

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

### <span data-ttu-id="73f63-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73f63-120">-InputObject</span></span>
<span data-ttu-id="73f63-121">Объект input</span><span class="sxs-lookup"><span data-stu-id="73f63-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73f63-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="73f63-122">-Name</span></span>
<span data-ttu-id="73f63-123">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="73f63-123">Resource Name</span></span>

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

### <span data-ttu-id="73f63-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="73f63-124">-PassThru</span></span>
<span data-ttu-id="73f63-125">Возвращает значение истина, если выполнено успешно</span><span class="sxs-lookup"><span data-stu-id="73f63-125">returns true if successful</span></span>

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

### <span data-ttu-id="73f63-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73f63-126">-ResourceGroupName</span></span>
<span data-ttu-id="73f63-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="73f63-127">Resource Group Name</span></span>

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

### <span data-ttu-id="73f63-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73f63-128">-ResourceId</span></span>
<span data-ttu-id="73f63-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="73f63-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="73f63-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="73f63-130">-Confirm</span></span>
<span data-ttu-id="73f63-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="73f63-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73f63-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73f63-132">-WhatIf</span></span>
<span data-ttu-id="73f63-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="73f63-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="73f63-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="73f63-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73f63-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73f63-135">CommonParameters</span></span>
<span data-ttu-id="73f63-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="73f63-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73f63-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="73f63-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73f63-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="73f63-138">INPUTS</span></span>

### <span data-ttu-id="73f63-139">System. String</span><span class="sxs-lookup"><span data-stu-id="73f63-139">System.String</span></span>

### <span data-ttu-id="73f63-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="73f63-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="73f63-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="73f63-141">OUTPUTS</span></span>

### <span data-ttu-id="73f63-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="73f63-142">System.Boolean</span></span>

## <span data-ttu-id="73f63-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="73f63-143">NOTES</span></span>

## <span data-ttu-id="73f63-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="73f63-144">RELATED LINKS</span></span>
