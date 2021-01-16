---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: 1a55a8c08182ae4a32e27bec74e4a5870aae95fa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410039"
---
# <span data-ttu-id="5df48-101">Remove-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="5df48-101">Remove-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="5df48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5df48-102">SYNOPSIS</span></span>
<span data-ttu-id="5df48-103">Удаляет учетные данные учетной записи хранения для устройства.</span><span class="sxs-lookup"><span data-stu-id="5df48-103">Removes a storage account credential for a device.</span></span>

## <span data-ttu-id="5df48-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5df48-104">SYNTAX</span></span>

### <span data-ttu-id="5df48-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5df48-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5df48-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5df48-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5df48-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5df48-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-InputObject] <PSStackEdgeStorageAccountCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5df48-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5df48-108">DESCRIPTION</span></span>
<span data-ttu-id="5df48-109">Cmdlet **Remove-AzStackEdgeStorageAccountCredential** удаляет учетные данные учетной записи хранения для устройства Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="5df48-109">The **Remove-AzStackEdgeStorageAccountCredential** cmdlet removes the storage account credential for a Stack Edge device.</span></span>

## <span data-ttu-id="5df48-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5df48-110">EXAMPLES</span></span>

### <span data-ttu-id="5df48-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5df48-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageAccountCredential ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAccountCredentialName
```

## <span data-ttu-id="5df48-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5df48-112">PARAMETERS</span></span>

### <span data-ttu-id="5df48-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5df48-113">-AsJob</span></span>
<span data-ttu-id="5df48-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5df48-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5df48-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5df48-115">-DefaultProfile</span></span>
<span data-ttu-id="5df48-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5df48-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5df48-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="5df48-117">-DeviceName</span></span>
<span data-ttu-id="5df48-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="5df48-118">Device Name</span></span>

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

### <span data-ttu-id="5df48-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5df48-119">-InputObject</span></span>
<span data-ttu-id="5df48-120">Объект Input</span><span class="sxs-lookup"><span data-stu-id="5df48-120">Input Object</span></span>

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

### <span data-ttu-id="5df48-121">-Name</span><span class="sxs-lookup"><span data-stu-id="5df48-121">-Name</span></span>
<span data-ttu-id="5df48-122">Имя используемой учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="5df48-122">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="5df48-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5df48-123">-PassThru</span></span>
<span data-ttu-id="5df48-124">возвращает "Истина" в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="5df48-124">returns true if successful</span></span>

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

### <span data-ttu-id="5df48-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5df48-125">-ResourceGroupName</span></span>
<span data-ttu-id="5df48-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="5df48-126">Resource Group Name</span></span>

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

### <span data-ttu-id="5df48-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5df48-127">-ResourceId</span></span>
<span data-ttu-id="5df48-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="5df48-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="5df48-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5df48-129">-Confirm</span></span>
<span data-ttu-id="5df48-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5df48-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5df48-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5df48-131">-WhatIf</span></span>
<span data-ttu-id="5df48-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5df48-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5df48-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5df48-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5df48-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5df48-134">CommonParameters</span></span>
<span data-ttu-id="5df48-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5df48-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5df48-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5df48-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5df48-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5df48-137">INPUTS</span></span>

### <span data-ttu-id="5df48-138">System.String</span><span class="sxs-lookup"><span data-stu-id="5df48-138">System.String</span></span>

### <span data-ttu-id="5df48-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="5df48-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="5df48-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5df48-140">OUTPUTS</span></span>

### <span data-ttu-id="5df48-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5df48-141">System.Boolean</span></span>

## <span data-ttu-id="5df48-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5df48-142">NOTES</span></span>

## <span data-ttu-id="5df48-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5df48-143">RELATED LINKS</span></span>
