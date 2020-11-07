---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDisk.md
ms.openlocfilehash: d48946b39c27a203e7d119c69e965633de8c6d6d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93913062"
---
# <span data-ttu-id="2c0bd-101">Remove-AzDisk</span><span class="sxs-lookup"><span data-stu-id="2c0bd-101">Remove-AzDisk</span></span>

## <span data-ttu-id="2c0bd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2c0bd-102">SYNOPSIS</span></span>
<span data-ttu-id="2c0bd-103">Удаление диска.</span><span class="sxs-lookup"><span data-stu-id="2c0bd-103">Removes a disk.</span></span>

## <span data-ttu-id="2c0bd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2c0bd-104">SYNTAX</span></span>

```
Remove-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c0bd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c0bd-105">DESCRIPTION</span></span>
<span data-ttu-id="2c0bd-106">Командлет **Remove-AzDisk** удаляет диск.</span><span class="sxs-lookup"><span data-stu-id="2c0bd-106">The **Remove-AzDisk** cmdlet removes a disk.</span></span>

## <span data-ttu-id="2c0bd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2c0bd-107">EXAMPLES</span></span>

### <span data-ttu-id="2c0bd-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2c0bd-108">Example 1</span></span>
```
PS C:\> Remove-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Force;
```

<span data-ttu-id="2c0bd-109">Эта команда удаляет диск с именем "Disk01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="2c0bd-109">This command removes the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="2c0bd-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2c0bd-110">PARAMETERS</span></span>

### <span data-ttu-id="2c0bd-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2c0bd-111">-AsJob</span></span>
<span data-ttu-id="2c0bd-112">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="2c0bd-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="2c0bd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c0bd-113">-DefaultProfile</span></span>
<span data-ttu-id="2c0bd-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2c0bd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c0bd-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="2c0bd-115">-DiskName</span></span>
<span data-ttu-id="2c0bd-116">Указывает имя диска.</span><span class="sxs-lookup"><span data-stu-id="2c0bd-116">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c0bd-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2c0bd-117">-Force</span></span>
<span data-ttu-id="2c0bd-118">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="2c0bd-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2c0bd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c0bd-119">-ResourceGroupName</span></span>
<span data-ttu-id="2c0bd-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2c0bd-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c0bd-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2c0bd-121">-Confirm</span></span>
<span data-ttu-id="2c0bd-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2c0bd-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c0bd-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c0bd-123">-WhatIf</span></span>
<span data-ttu-id="2c0bd-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2c0bd-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c0bd-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2c0bd-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c0bd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c0bd-126">CommonParameters</span></span>
<span data-ttu-id="2c0bd-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2c0bd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c0bd-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c0bd-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c0bd-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2c0bd-129">INPUTS</span></span>

### <span data-ttu-id="2c0bd-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2c0bd-130">System.String</span></span>

## <span data-ttu-id="2c0bd-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c0bd-131">OUTPUTS</span></span>

### <span data-ttu-id="2c0bd-132">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="2c0bd-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="2c0bd-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="2c0bd-133">NOTES</span></span>

## <span data-ttu-id="2c0bd-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2c0bd-134">RELATED LINKS</span></span>
