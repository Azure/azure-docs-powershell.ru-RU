---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzSnapshot.md
ms.openlocfilehash: 686f7dbe4bba17017e1920dd2c67a05c2ccd5eae
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414247"
---
# <span data-ttu-id="6eb93-101">Remove-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="6eb93-101">Remove-AzSnapshot</span></span>

## <span data-ttu-id="6eb93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6eb93-102">SYNOPSIS</span></span>
<span data-ttu-id="6eb93-103">Удаляет моментальный снимок.</span><span class="sxs-lookup"><span data-stu-id="6eb93-103">Removes a snapshot.</span></span>

## <span data-ttu-id="6eb93-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6eb93-104">SYNTAX</span></span>

```
Remove-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6eb93-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6eb93-105">DESCRIPTION</span></span>
<span data-ttu-id="6eb93-106">Для **удаления снимка удаляется cmdlet Remove-AzSnapshot.**</span><span class="sxs-lookup"><span data-stu-id="6eb93-106">The **Remove-AzSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="6eb93-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6eb93-107">EXAMPLES</span></span>

### <span data-ttu-id="6eb93-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6eb93-108">Example 1</span></span>
```
PS C:\> Remove-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="6eb93-109">Эта команда удаляет моментальный снимок с именем "Моментальный снимок01" в группе ресурсов "Группа ресурсов01".</span><span class="sxs-lookup"><span data-stu-id="6eb93-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="6eb93-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6eb93-110">PARAMETERS</span></span>

### <span data-ttu-id="6eb93-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6eb93-111">-AsJob</span></span>
<span data-ttu-id="6eb93-112">Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="6eb93-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="6eb93-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eb93-113">-DefaultProfile</span></span>
<span data-ttu-id="6eb93-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6eb93-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6eb93-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6eb93-115">-Force</span></span>
<span data-ttu-id="6eb93-116">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="6eb93-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6eb93-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6eb93-117">-ResourceGroupName</span></span>
<span data-ttu-id="6eb93-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6eb93-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="6eb93-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="6eb93-119">-SnapshotName</span></span>
<span data-ttu-id="6eb93-120">Указывает имя моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="6eb93-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="6eb93-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6eb93-121">-Confirm</span></span>
<span data-ttu-id="6eb93-122">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="6eb93-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6eb93-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6eb93-123">-WhatIf</span></span>
<span data-ttu-id="6eb93-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6eb93-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6eb93-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6eb93-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6eb93-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eb93-126">CommonParameters</span></span>
<span data-ttu-id="6eb93-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6eb93-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eb93-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6eb93-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eb93-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6eb93-129">INPUTS</span></span>

### <span data-ttu-id="6eb93-130">System.String</span><span class="sxs-lookup"><span data-stu-id="6eb93-130">System.String</span></span>

## <span data-ttu-id="6eb93-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6eb93-131">OUTPUTS</span></span>

### <span data-ttu-id="6eb93-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="6eb93-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="6eb93-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6eb93-133">NOTES</span></span>

## <span data-ttu-id="6eb93-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6eb93-134">RELATED LINKS</span></span>
