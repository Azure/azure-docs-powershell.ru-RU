---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
ms.openlocfilehash: a15dd51bad097aafcc517fbef67f89d65b076380
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079797"
---
# <span data-ttu-id="6151a-101">Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="6151a-101">Remove-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="6151a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6151a-102">SYNOPSIS</span></span>
<span data-ttu-id="6151a-103">Удаляет набор шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="6151a-103">Removes a disk encryption set.</span></span>

## <span data-ttu-id="6151a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6151a-104">SYNTAX</span></span>

### <span data-ttu-id="6151a-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6151a-105">DefaultParameter (Default)</span></span>
```
Remove-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6151a-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="6151a-106">ResourceIdParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6151a-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="6151a-107">ObjectParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-InputObject] <PSDiskEncryptionSet> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6151a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6151a-108">DESCRIPTION</span></span>
<span data-ttu-id="6151a-109">Удаляет набор шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="6151a-109">Removes a disk encryption set.</span></span>

## <span data-ttu-id="6151a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6151a-110">EXAMPLES</span></span>

### <span data-ttu-id="6151a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6151a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -Force;
```

<span data-ttu-id="6151a-112">Удалить параметр "enc1" в "Rg1" для шифрования диска</span><span class="sxs-lookup"><span data-stu-id="6151a-112">Delete disk encryption set 'enc1' in 'rg1'</span></span>

## <span data-ttu-id="6151a-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6151a-113">PARAMETERS</span></span>

### <span data-ttu-id="6151a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6151a-114">-AsJob</span></span>
<span data-ttu-id="6151a-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6151a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6151a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6151a-116">-DefaultProfile</span></span>
<span data-ttu-id="6151a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6151a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6151a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="6151a-118">-Force</span></span>
<span data-ttu-id="6151a-119">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="6151a-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6151a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6151a-120">-InputObject</span></span>
<span data-ttu-id="6151a-121">Локальный объект набора шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="6151a-121">The local object of the disk encryption set.</span></span>

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

### <span data-ttu-id="6151a-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6151a-122">-Name</span></span>
<span data-ttu-id="6151a-123">Имя набора шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="6151a-123">Name of disk encryption set.</span></span>

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

### <span data-ttu-id="6151a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6151a-124">-ResourceGroupName</span></span>
<span data-ttu-id="6151a-125">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6151a-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="6151a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6151a-126">-ResourceId</span></span>
<span data-ttu-id="6151a-127">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="6151a-127">The ID of the resource.</span></span>

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

### <span data-ttu-id="6151a-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6151a-128">-Confirm</span></span>
<span data-ttu-id="6151a-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6151a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6151a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6151a-130">-WhatIf</span></span>
<span data-ttu-id="6151a-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6151a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6151a-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6151a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6151a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6151a-133">CommonParameters</span></span>
<span data-ttu-id="6151a-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6151a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6151a-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6151a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6151a-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6151a-136">INPUTS</span></span>

### <span data-ttu-id="6151a-137">System. String</span><span class="sxs-lookup"><span data-stu-id="6151a-137">System.String</span></span>

### <span data-ttu-id="6151a-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="6151a-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="6151a-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6151a-139">OUTPUTS</span></span>

### <span data-ttu-id="6151a-140">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="6151a-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="6151a-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="6151a-141">NOTES</span></span>

## <span data-ttu-id="6151a-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6151a-142">RELATED LINKS</span></span>
