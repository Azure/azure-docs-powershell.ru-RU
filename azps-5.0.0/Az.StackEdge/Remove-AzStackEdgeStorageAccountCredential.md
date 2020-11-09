---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: 1a55a8c08182ae4a32e27bec74e4a5870aae95fa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317531"
---
# <span data-ttu-id="d17ea-101">Remove-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="d17ea-101">Remove-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="d17ea-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d17ea-102">SYNOPSIS</span></span>
<span data-ttu-id="d17ea-103">Удаление учетных данных учетной записи хранения для устройства.</span><span class="sxs-lookup"><span data-stu-id="d17ea-103">Removes a storage account credential for a device.</span></span>

## <span data-ttu-id="d17ea-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d17ea-104">SYNTAX</span></span>

### <span data-ttu-id="d17ea-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d17ea-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d17ea-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d17ea-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d17ea-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d17ea-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-InputObject] <PSStackEdgeStorageAccountCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d17ea-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d17ea-108">DESCRIPTION</span></span>
<span data-ttu-id="d17ea-109">Командлет **Remove-AzStackEdgeStorageAccountCredential** удаляет учетные данные учетной записи хранения для краевого устройства стека.</span><span class="sxs-lookup"><span data-stu-id="d17ea-109">The **Remove-AzStackEdgeStorageAccountCredential** cmdlet removes the storage account credential for a Stack Edge device.</span></span>

## <span data-ttu-id="d17ea-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d17ea-110">EXAMPLES</span></span>

### <span data-ttu-id="d17ea-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d17ea-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageAccountCredential ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAccountCredentialName
```

## <span data-ttu-id="d17ea-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d17ea-112">PARAMETERS</span></span>

### <span data-ttu-id="d17ea-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d17ea-113">-AsJob</span></span>
<span data-ttu-id="d17ea-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d17ea-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d17ea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d17ea-115">-DefaultProfile</span></span>
<span data-ttu-id="d17ea-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d17ea-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d17ea-117">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="d17ea-117">-DeviceName</span></span>
<span data-ttu-id="d17ea-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="d17ea-118">Device Name</span></span>

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

### <span data-ttu-id="d17ea-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d17ea-119">-InputObject</span></span>
<span data-ttu-id="d17ea-120">Объект input</span><span class="sxs-lookup"><span data-stu-id="d17ea-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: StorageAccountCredential

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d17ea-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d17ea-121">-Name</span></span>
<span data-ttu-id="d17ea-122">Имя учетной записи хранения, которую нужно использовать</span><span class="sxs-lookup"><span data-stu-id="d17ea-122">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d17ea-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d17ea-123">-PassThru</span></span>
<span data-ttu-id="d17ea-124">Возвращает значение истина, если выполнено успешно</span><span class="sxs-lookup"><span data-stu-id="d17ea-124">returns true if successful</span></span>

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

### <span data-ttu-id="d17ea-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d17ea-125">-ResourceGroupName</span></span>
<span data-ttu-id="d17ea-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="d17ea-126">Resource Group Name</span></span>

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

### <span data-ttu-id="d17ea-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d17ea-127">-ResourceId</span></span>
<span data-ttu-id="d17ea-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="d17ea-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="d17ea-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d17ea-129">-Confirm</span></span>
<span data-ttu-id="d17ea-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d17ea-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d17ea-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d17ea-131">-WhatIf</span></span>
<span data-ttu-id="d17ea-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d17ea-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d17ea-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d17ea-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d17ea-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d17ea-134">CommonParameters</span></span>
<span data-ttu-id="d17ea-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d17ea-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d17ea-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d17ea-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d17ea-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d17ea-137">INPUTS</span></span>

### <span data-ttu-id="d17ea-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d17ea-138">System.String</span></span>

### <span data-ttu-id="d17ea-139">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="d17ea-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="d17ea-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d17ea-140">OUTPUTS</span></span>

### <span data-ttu-id="d17ea-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d17ea-141">System.Boolean</span></span>

## <span data-ttu-id="d17ea-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="d17ea-142">NOTES</span></span>

## <span data-ttu-id="d17ea-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d17ea-143">RELATED LINKS</span></span>
