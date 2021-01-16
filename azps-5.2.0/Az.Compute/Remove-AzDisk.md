---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDisk.md
ms.openlocfilehash: d48946b39c27a203e7d119c69e965633de8c6d6d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402796"
---
# <span data-ttu-id="ad588-101">Remove-AzDisk</span><span class="sxs-lookup"><span data-stu-id="ad588-101">Remove-AzDisk</span></span>

## <span data-ttu-id="ad588-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad588-102">SYNOPSIS</span></span>
<span data-ttu-id="ad588-103">Удаляет диск.</span><span class="sxs-lookup"><span data-stu-id="ad588-103">Removes a disk.</span></span>

## <span data-ttu-id="ad588-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ad588-104">SYNTAX</span></span>

```
Remove-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad588-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad588-105">DESCRIPTION</span></span>
<span data-ttu-id="ad588-106">Для **удаления диска удаляется cmdlet Remove-AzDisk.**</span><span class="sxs-lookup"><span data-stu-id="ad588-106">The **Remove-AzDisk** cmdlet removes a disk.</span></span>

## <span data-ttu-id="ad588-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ad588-107">EXAMPLES</span></span>

### <span data-ttu-id="ad588-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ad588-108">Example 1</span></span>
```
PS C:\> Remove-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Force;
```

<span data-ttu-id="ad588-109">Эта команда удаляет диск "Диск01" в группе ресурсов "Группа ресурсов01".</span><span class="sxs-lookup"><span data-stu-id="ad588-109">This command removes the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="ad588-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad588-110">PARAMETERS</span></span>

### <span data-ttu-id="ad588-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad588-111">-AsJob</span></span>
<span data-ttu-id="ad588-112">Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="ad588-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="ad588-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad588-113">-DefaultProfile</span></span>
<span data-ttu-id="ad588-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ad588-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad588-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="ad588-115">-DiskName</span></span>
<span data-ttu-id="ad588-116">Указывает имя диска.</span><span class="sxs-lookup"><span data-stu-id="ad588-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="ad588-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ad588-117">-Force</span></span>
<span data-ttu-id="ad588-118">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="ad588-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ad588-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad588-119">-ResourceGroupName</span></span>
<span data-ttu-id="ad588-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ad588-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ad588-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad588-121">-Confirm</span></span>
<span data-ttu-id="ad588-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad588-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad588-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad588-123">-WhatIf</span></span>
<span data-ttu-id="ad588-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad588-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad588-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ad588-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad588-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad588-126">CommonParameters</span></span>
<span data-ttu-id="ad588-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad588-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad588-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ad588-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad588-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ad588-129">INPUTS</span></span>

### <span data-ttu-id="ad588-130">System.String</span><span class="sxs-lookup"><span data-stu-id="ad588-130">System.String</span></span>

## <span data-ttu-id="ad588-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ad588-131">OUTPUTS</span></span>

### <span data-ttu-id="ad588-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="ad588-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="ad588-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ad588-133">NOTES</span></span>

## <span data-ttu-id="ad588-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ad588-134">RELATED LINKS</span></span>