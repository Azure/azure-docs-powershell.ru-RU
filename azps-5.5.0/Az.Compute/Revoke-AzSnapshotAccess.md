---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/revoke-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
ms.openlocfilehash: 35e767c340d5418ae500c4cc87a4b40741d8ba6a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238743"
---
# <span data-ttu-id="63d99-101">Revoke-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="63d99-101">Revoke-AzSnapshotAccess</span></span>

## <span data-ttu-id="63d99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63d99-102">SYNOPSIS</span></span>
<span data-ttu-id="63d99-103">Отзыв доступа к моментального снимку.</span><span class="sxs-lookup"><span data-stu-id="63d99-103">Revokes an access to a snapshot.</span></span>

## <span data-ttu-id="63d99-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="63d99-104">SYNTAX</span></span>

```
Revoke-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63d99-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="63d99-105">DESCRIPTION</span></span>
<span data-ttu-id="63d99-106">**Cmdlet Revoke-AzSnapshotAccess** отзывает доступ к снимку.</span><span class="sxs-lookup"><span data-stu-id="63d99-106">The **Revoke-AzSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="63d99-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="63d99-107">EXAMPLES</span></span>

### <span data-ttu-id="63d99-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="63d99-108">Example 1</span></span>
```
PS C:\> Revoke-AzSnapshotAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="63d99-109">Отощут доступ к моментального снимку с именем "Моментальный снимок01" в группе ресурсов "Группа ресурсов01"</span><span class="sxs-lookup"><span data-stu-id="63d99-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="63d99-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="63d99-110">PARAMETERS</span></span>

### <span data-ttu-id="63d99-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="63d99-111">-AsJob</span></span>
<span data-ttu-id="63d99-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="63d99-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="63d99-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63d99-113">-DefaultProfile</span></span>
<span data-ttu-id="63d99-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="63d99-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63d99-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63d99-115">-ResourceGroupName</span></span>
<span data-ttu-id="63d99-116">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="63d99-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="63d99-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="63d99-117">-SnapshotName</span></span>
<span data-ttu-id="63d99-118">Указывает имя моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="63d99-118">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="63d99-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="63d99-119">-Confirm</span></span>
<span data-ttu-id="63d99-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="63d99-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63d99-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63d99-121">-WhatIf</span></span>
<span data-ttu-id="63d99-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63d99-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="63d99-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="63d99-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63d99-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63d99-124">CommonParameters</span></span>
<span data-ttu-id="63d99-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63d99-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63d99-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="63d99-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63d99-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="63d99-127">INPUTS</span></span>

### <span data-ttu-id="63d99-128">System.String</span><span class="sxs-lookup"><span data-stu-id="63d99-128">System.String</span></span>

## <span data-ttu-id="63d99-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="63d99-129">OUTPUTS</span></span>

### <span data-ttu-id="63d99-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="63d99-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="63d99-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="63d99-131">NOTES</span></span>

## <span data-ttu-id="63d99-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="63d99-132">RELATED LINKS</span></span>
