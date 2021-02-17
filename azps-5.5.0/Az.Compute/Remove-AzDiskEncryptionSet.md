---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
ms.openlocfilehash: a15dd51bad097aafcc517fbef67f89d65b076380
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238816"
---
# <span data-ttu-id="b6469-101">Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="b6469-101">Remove-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="b6469-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6469-102">SYNOPSIS</span></span>
<span data-ttu-id="b6469-103">Удаляет набор шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="b6469-103">Removes a disk encryption set.</span></span>

## <span data-ttu-id="b6469-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b6469-104">SYNTAX</span></span>

### <span data-ttu-id="b6469-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b6469-105">DefaultParameter (Default)</span></span>
```
Remove-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6469-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="b6469-106">ResourceIdParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6469-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="b6469-107">ObjectParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-InputObject] <PSDiskEncryptionSet> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6469-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6469-108">DESCRIPTION</span></span>
<span data-ttu-id="b6469-109">Удаляет набор шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="b6469-109">Removes a disk encryption set.</span></span>

## <span data-ttu-id="b6469-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b6469-110">EXAMPLES</span></span>

### <span data-ttu-id="b6469-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b6469-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -Force;
```

<span data-ttu-id="b6469-112">Удаление набора шифрования диска (enc1) в "rg1"</span><span class="sxs-lookup"><span data-stu-id="b6469-112">Delete disk encryption set 'enc1' in 'rg1'</span></span>

## <span data-ttu-id="b6469-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6469-113">PARAMETERS</span></span>

### <span data-ttu-id="b6469-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6469-114">-AsJob</span></span>
<span data-ttu-id="b6469-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b6469-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b6469-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6469-116">-DefaultProfile</span></span>
<span data-ttu-id="b6469-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b6469-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6469-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b6469-118">-Force</span></span>
<span data-ttu-id="b6469-119">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="b6469-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b6469-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6469-120">-InputObject</span></span>
<span data-ttu-id="b6469-121">Локальный объект набора шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="b6469-121">The local object of the disk encryption set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet
Parameter Sets: ObjectParameter
Aliases: DiskEncryptionSet

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6469-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b6469-122">-Name</span></span>
<span data-ttu-id="b6469-123">Имя набора шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="b6469-123">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: DiskEncryptionSetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6469-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6469-124">-ResourceGroupName</span></span>
<span data-ttu-id="b6469-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b6469-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6469-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6469-126">-ResourceId</span></span>
<span data-ttu-id="b6469-127">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="b6469-127">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6469-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6469-128">-Confirm</span></span>
<span data-ttu-id="b6469-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="b6469-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6469-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6469-130">-WhatIf</span></span>
<span data-ttu-id="b6469-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6469-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6469-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b6469-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6469-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6469-133">CommonParameters</span></span>
<span data-ttu-id="b6469-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6469-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6469-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b6469-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6469-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b6469-136">INPUTS</span></span>

### <span data-ttu-id="b6469-137">System.String</span><span class="sxs-lookup"><span data-stu-id="b6469-137">System.String</span></span>

### <span data-ttu-id="b6469-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="b6469-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="b6469-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b6469-139">OUTPUTS</span></span>

### <span data-ttu-id="b6469-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="b6469-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="b6469-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b6469-141">NOTES</span></span>

## <span data-ttu-id="b6469-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b6469-142">RELATED LINKS</span></span>
