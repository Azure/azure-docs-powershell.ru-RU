---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/grant-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
ms.openlocfilehash: 215ae1149cdfd939db242907a00b82b1e9fd82a2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001752"
---
# <span data-ttu-id="4904d-101">Grant-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="4904d-101">Grant-AzSnapshotAccess</span></span>

## <span data-ttu-id="4904d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4904d-102">SYNOPSIS</span></span>
<span data-ttu-id="4904d-103">Предоставляет доступ к моментального снимку.</span><span class="sxs-lookup"><span data-stu-id="4904d-103">Grants an access to a snapshot.</span></span>

## <span data-ttu-id="4904d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4904d-104">SYNTAX</span></span>

```
Grant-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4904d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4904d-105">DESCRIPTION</span></span>
<span data-ttu-id="4904d-106">С **его учетом** можно получить доступ к снимку.</span><span class="sxs-lookup"><span data-stu-id="4904d-106">The **Grant-AzSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="4904d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4904d-107">EXAMPLES</span></span>

### <span data-ttu-id="4904d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4904d-108">Example 1</span></span>
```
PS C:\> Grant-AzSnapshotAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="4904d-109">Предоставить доступ "Чтение" к моментального снимку "Моментальный снимок01" в группе ресурсов "Группа ресурсов01" в течение 60 секунд.</span><span class="sxs-lookup"><span data-stu-id="4904d-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="4904d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4904d-110">PARAMETERS</span></span>

### <span data-ttu-id="4904d-111">-Access</span><span class="sxs-lookup"><span data-stu-id="4904d-111">-Access</span></span>
<span data-ttu-id="4904d-112">Определяет уровень доступа.</span><span class="sxs-lookup"><span data-stu-id="4904d-112">Specifies Access level.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4904d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4904d-113">-AsJob</span></span>
<span data-ttu-id="4904d-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="4904d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4904d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4904d-115">-DefaultProfile</span></span>
<span data-ttu-id="4904d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4904d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4904d-117">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="4904d-117">-DurationInSecond</span></span>
<span data-ttu-id="4904d-118">Определяет длительность доступа в секундах.</span><span class="sxs-lookup"><span data-stu-id="4904d-118">Specifies access duration in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4904d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4904d-119">-ResourceGroupName</span></span>
<span data-ttu-id="4904d-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4904d-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4904d-121">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="4904d-121">-SnapshotName</span></span>
<span data-ttu-id="4904d-122">Указывает имя моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="4904d-122">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="4904d-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4904d-123">-Confirm</span></span>
<span data-ttu-id="4904d-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="4904d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4904d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4904d-125">-WhatIf</span></span>
<span data-ttu-id="4904d-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4904d-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4904d-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4904d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4904d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4904d-128">CommonParameters</span></span>
<span data-ttu-id="4904d-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4904d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4904d-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4904d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4904d-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4904d-131">INPUTS</span></span>

### <span data-ttu-id="4904d-132">System.String</span><span class="sxs-lookup"><span data-stu-id="4904d-132">System.String</span></span>

## <span data-ttu-id="4904d-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4904d-133">OUTPUTS</span></span>

### <span data-ttu-id="4904d-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span><span class="sxs-lookup"><span data-stu-id="4904d-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="4904d-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4904d-135">NOTES</span></span>

## <span data-ttu-id="4904d-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4904d-136">RELATED LINKS</span></span>
