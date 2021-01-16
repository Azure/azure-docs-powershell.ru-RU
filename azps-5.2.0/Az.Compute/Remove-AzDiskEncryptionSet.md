---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
ms.openlocfilehash: a15dd51bad097aafcc517fbef67f89d65b076380
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414780"
---
# <span data-ttu-id="927cc-101">Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="927cc-101">Remove-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="927cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="927cc-102">SYNOPSIS</span></span>
<span data-ttu-id="927cc-103">Удаляет набор шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="927cc-103">Removes a disk encryption set.</span></span>

## <span data-ttu-id="927cc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="927cc-104">SYNTAX</span></span>

### <span data-ttu-id="927cc-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="927cc-105">DefaultParameter (Default)</span></span>
```
Remove-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="927cc-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="927cc-106">ResourceIdParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="927cc-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="927cc-107">ObjectParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-InputObject] <PSDiskEncryptionSet> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="927cc-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="927cc-108">DESCRIPTION</span></span>
<span data-ttu-id="927cc-109">Удаляет набор шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="927cc-109">Removes a disk encryption set.</span></span>

## <span data-ttu-id="927cc-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="927cc-110">EXAMPLES</span></span>

### <span data-ttu-id="927cc-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="927cc-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -Force;
```

<span data-ttu-id="927cc-112">Удаление набора шифрования диска (enc1) в "rg1"</span><span class="sxs-lookup"><span data-stu-id="927cc-112">Delete disk encryption set 'enc1' in 'rg1'</span></span>

## <span data-ttu-id="927cc-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="927cc-113">PARAMETERS</span></span>

### <span data-ttu-id="927cc-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="927cc-114">-AsJob</span></span>
<span data-ttu-id="927cc-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="927cc-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="927cc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="927cc-116">-DefaultProfile</span></span>
<span data-ttu-id="927cc-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="927cc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="927cc-118">-Force</span><span class="sxs-lookup"><span data-stu-id="927cc-118">-Force</span></span>
<span data-ttu-id="927cc-119">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="927cc-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="927cc-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="927cc-120">-InputObject</span></span>
<span data-ttu-id="927cc-121">Локальный объект набора шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="927cc-121">The local object of the disk encryption set.</span></span>

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

### <span data-ttu-id="927cc-122">-Name</span><span class="sxs-lookup"><span data-stu-id="927cc-122">-Name</span></span>
<span data-ttu-id="927cc-123">Имя набора шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="927cc-123">Name of disk encryption set.</span></span>

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

### <span data-ttu-id="927cc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="927cc-124">-ResourceGroupName</span></span>
<span data-ttu-id="927cc-125">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="927cc-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="927cc-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="927cc-126">-ResourceId</span></span>
<span data-ttu-id="927cc-127">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="927cc-127">The ID of the resource.</span></span>

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

### <span data-ttu-id="927cc-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="927cc-128">-Confirm</span></span>
<span data-ttu-id="927cc-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="927cc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="927cc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="927cc-130">-WhatIf</span></span>
<span data-ttu-id="927cc-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="927cc-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="927cc-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="927cc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="927cc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="927cc-133">CommonParameters</span></span>
<span data-ttu-id="927cc-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="927cc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="927cc-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="927cc-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="927cc-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="927cc-136">INPUTS</span></span>

### <span data-ttu-id="927cc-137">System.String</span><span class="sxs-lookup"><span data-stu-id="927cc-137">System.String</span></span>

### <span data-ttu-id="927cc-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="927cc-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="927cc-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="927cc-139">OUTPUTS</span></span>

### <span data-ttu-id="927cc-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="927cc-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="927cc-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="927cc-141">NOTES</span></span>

## <span data-ttu-id="927cc-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="927cc-142">RELATED LINKS</span></span>
