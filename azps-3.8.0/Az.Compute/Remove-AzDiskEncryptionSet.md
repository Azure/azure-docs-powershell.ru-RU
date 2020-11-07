---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
ms.openlocfilehash: a15dd51bad097aafcc517fbef67f89d65b076380
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93913052"
---
# <span data-ttu-id="04d99-101">Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="04d99-101">Remove-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="04d99-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="04d99-102">SYNOPSIS</span></span>
<span data-ttu-id="04d99-103">Удаляет набор шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="04d99-103">Removes a disk encryption set.</span></span>

## <span data-ttu-id="04d99-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="04d99-104">SYNTAX</span></span>

### <span data-ttu-id="04d99-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="04d99-105">DefaultParameter (Default)</span></span>
```
Remove-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04d99-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="04d99-106">ResourceIdParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04d99-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="04d99-107">ObjectParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-InputObject] <PSDiskEncryptionSet> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04d99-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="04d99-108">DESCRIPTION</span></span>
<span data-ttu-id="04d99-109">Удаляет набор шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="04d99-109">Removes a disk encryption set.</span></span>

## <span data-ttu-id="04d99-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="04d99-110">EXAMPLES</span></span>

### <span data-ttu-id="04d99-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="04d99-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -Force;
```

<span data-ttu-id="04d99-112">Удалить параметр "enc1" в "Rg1" для шифрования диска</span><span class="sxs-lookup"><span data-stu-id="04d99-112">Delete disk encryption set 'enc1' in 'rg1'</span></span>

## <span data-ttu-id="04d99-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="04d99-113">PARAMETERS</span></span>

### <span data-ttu-id="04d99-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04d99-114">-AsJob</span></span>
<span data-ttu-id="04d99-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="04d99-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="04d99-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04d99-116">-DefaultProfile</span></span>
<span data-ttu-id="04d99-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="04d99-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04d99-118">-Force</span><span class="sxs-lookup"><span data-stu-id="04d99-118">-Force</span></span>
<span data-ttu-id="04d99-119">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="04d99-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="04d99-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04d99-120">-InputObject</span></span>
<span data-ttu-id="04d99-121">Локальный объект набора шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="04d99-121">The local object of the disk encryption set.</span></span>

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

### <span data-ttu-id="04d99-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="04d99-122">-Name</span></span>
<span data-ttu-id="04d99-123">Имя набора шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="04d99-123">Name of disk encryption set.</span></span>

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

### <span data-ttu-id="04d99-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04d99-124">-ResourceGroupName</span></span>
<span data-ttu-id="04d99-125">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="04d99-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="04d99-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="04d99-126">-ResourceId</span></span>
<span data-ttu-id="04d99-127">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="04d99-127">The ID of the resource.</span></span>

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

### <span data-ttu-id="04d99-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="04d99-128">-Confirm</span></span>
<span data-ttu-id="04d99-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="04d99-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04d99-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04d99-130">-WhatIf</span></span>
<span data-ttu-id="04d99-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="04d99-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04d99-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="04d99-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04d99-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04d99-133">CommonParameters</span></span>
<span data-ttu-id="04d99-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="04d99-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04d99-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04d99-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04d99-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="04d99-136">INPUTS</span></span>

### <span data-ttu-id="04d99-137">System. String</span><span class="sxs-lookup"><span data-stu-id="04d99-137">System.String</span></span>

### <span data-ttu-id="04d99-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="04d99-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="04d99-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="04d99-139">OUTPUTS</span></span>

### <span data-ttu-id="04d99-140">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="04d99-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="04d99-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="04d99-141">NOTES</span></span>

## <span data-ttu-id="04d99-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="04d99-142">RELATED LINKS</span></span>
