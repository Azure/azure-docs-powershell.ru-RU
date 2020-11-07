---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/revoke-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
ms.openlocfilehash: 5ce2d21ecf0669bd5babc92f4b1fa514480bd639
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721732"
---
# <span data-ttu-id="4f9ff-101">Revoke-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="4f9ff-101">Revoke-AzSnapshotAccess</span></span>

## <span data-ttu-id="4f9ff-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4f9ff-102">SYNOPSIS</span></span>
<span data-ttu-id="4f9ff-103">Отменяет доступ к снимку.</span><span class="sxs-lookup"><span data-stu-id="4f9ff-103">Revokes an access to a snapshot.</span></span>

## <span data-ttu-id="4f9ff-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4f9ff-104">SYNTAX</span></span>

```
Revoke-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f9ff-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4f9ff-105">DESCRIPTION</span></span>
<span data-ttu-id="4f9ff-106">Командлет **REVOKE-AzSnapshotAccess** отменяет доступ к моментальному снимку.</span><span class="sxs-lookup"><span data-stu-id="4f9ff-106">The **Revoke-AzSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="4f9ff-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4f9ff-107">EXAMPLES</span></span>

### <span data-ttu-id="4f9ff-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4f9ff-108">Example 1</span></span>
```
PS C:\> Revoke-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="4f9ff-109">Отмена доступа к моментальному снимку с именем "Snapshot01" в группе ресурсов с именем "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="4f9ff-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="4f9ff-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4f9ff-110">PARAMETERS</span></span>

### <span data-ttu-id="4f9ff-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4f9ff-111">-AsJob</span></span>
<span data-ttu-id="4f9ff-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="4f9ff-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4f9ff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f9ff-113">-DefaultProfile</span></span>
<span data-ttu-id="4f9ff-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4f9ff-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f9ff-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f9ff-115">-ResourceGroupName</span></span>
<span data-ttu-id="4f9ff-116">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4f9ff-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4f9ff-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="4f9ff-117">-SnapshotName</span></span>
<span data-ttu-id="4f9ff-118">Указывает имя снимка.</span><span class="sxs-lookup"><span data-stu-id="4f9ff-118">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="4f9ff-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4f9ff-119">-Confirm</span></span>
<span data-ttu-id="4f9ff-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4f9ff-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f9ff-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f9ff-121">-WhatIf</span></span>
<span data-ttu-id="4f9ff-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4f9ff-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4f9ff-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4f9ff-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f9ff-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f9ff-124">CommonParameters</span></span>
<span data-ttu-id="4f9ff-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4f9ff-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f9ff-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4f9ff-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f9ff-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4f9ff-127">INPUTS</span></span>

### <span data-ttu-id="4f9ff-128">System. String</span><span class="sxs-lookup"><span data-stu-id="4f9ff-128">System.String</span></span>

## <span data-ttu-id="4f9ff-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4f9ff-129">OUTPUTS</span></span>

### <span data-ttu-id="4f9ff-130">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="4f9ff-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="4f9ff-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="4f9ff-131">NOTES</span></span>

## <span data-ttu-id="4f9ff-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4f9ff-132">RELATED LINKS</span></span>
