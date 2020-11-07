---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: dff83dbb7183c4f9eaf46e883a92a8e615f9cacc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911249"
---
# <span data-ttu-id="f4257-101">Remove-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="f4257-101">Remove-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="f4257-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f4257-102">SYNOPSIS</span></span>
<span data-ttu-id="f4257-103">Удаление учетных данных учетной записи хранения для устройства.</span><span class="sxs-lookup"><span data-stu-id="f4257-103">Removes a storage account credential for a device.</span></span>

## <span data-ttu-id="f4257-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f4257-104">SYNTAX</span></span>

### <span data-ttu-id="f4257-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f4257-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f4257-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4257-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccountCredential [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4257-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4257-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccountCredential [-InputObject] <PSDataBoxEdgeStorageAccountCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4257-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4257-108">DESCRIPTION</span></span>
<span data-ttu-id="f4257-109">Командлет **Remove-AzDataBoxEdgeStorageAccountCredential** удаляет учетные данные учетной записи хранения на пограничном устройстве поля данных.</span><span class="sxs-lookup"><span data-stu-id="f4257-109">The **Remove-AzDataBoxEdgeStorageAccountCredential** cmdlet removes the storage account credential for a Data Box Edge device.</span></span>

## <span data-ttu-id="f4257-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f4257-110">EXAMPLES</span></span>

### <span data-ttu-id="f4257-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f4257-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeStorageAccountCredential ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAccountCredentialName
```

## <span data-ttu-id="f4257-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f4257-112">PARAMETERS</span></span>

### <span data-ttu-id="f4257-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4257-113">-AsJob</span></span>
<span data-ttu-id="f4257-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f4257-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f4257-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4257-115">-DefaultProfile</span></span>
<span data-ttu-id="f4257-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f4257-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4257-117">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="f4257-117">-DeviceName</span></span>
<span data-ttu-id="f4257-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="f4257-118">Device Name</span></span>

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

### <span data-ttu-id="f4257-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4257-119">-InputObject</span></span>
<span data-ttu-id="f4257-120">Объект input</span><span class="sxs-lookup"><span data-stu-id="f4257-120">Input Object</span></span>

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

### <span data-ttu-id="f4257-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f4257-121">-Name</span></span>
<span data-ttu-id="f4257-122">Имя учетной записи хранения, которую нужно использовать</span><span class="sxs-lookup"><span data-stu-id="f4257-122">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="f4257-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f4257-123">-PassThru</span></span>
<span data-ttu-id="f4257-124">Возвращает значение истина, если выполнено успешно</span><span class="sxs-lookup"><span data-stu-id="f4257-124">returns true if successful</span></span>

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

### <span data-ttu-id="f4257-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4257-125">-ResourceGroupName</span></span>
<span data-ttu-id="f4257-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f4257-126">Resource Group Name</span></span>

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

### <span data-ttu-id="f4257-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4257-127">-ResourceId</span></span>
<span data-ttu-id="f4257-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4257-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="f4257-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4257-129">-Confirm</span></span>
<span data-ttu-id="f4257-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f4257-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4257-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4257-131">-WhatIf</span></span>
<span data-ttu-id="f4257-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f4257-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4257-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f4257-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4257-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4257-134">CommonParameters</span></span>
<span data-ttu-id="f4257-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f4257-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4257-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f4257-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4257-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f4257-137">INPUTS</span></span>

### <span data-ttu-id="f4257-138">System. String</span><span class="sxs-lookup"><span data-stu-id="f4257-138">System.String</span></span>

### <span data-ttu-id="f4257-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="f4257-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="f4257-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4257-140">OUTPUTS</span></span>

### <span data-ttu-id="f4257-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f4257-141">System.Boolean</span></span>

## <span data-ttu-id="f4257-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="f4257-142">NOTES</span></span>

## <span data-ttu-id="f4257-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f4257-143">RELATED LINKS</span></span>
