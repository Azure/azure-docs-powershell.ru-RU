---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/revoke-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
ms.openlocfilehash: 35e767c340d5418ae500c4cc87a4b40741d8ba6a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94080020"
---
# <span data-ttu-id="ee4f8-101">Revoke-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="ee4f8-101">Revoke-AzSnapshotAccess</span></span>

## <span data-ttu-id="ee4f8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ee4f8-102">SYNOPSIS</span></span>
<span data-ttu-id="ee4f8-103">Отменяет доступ к снимку.</span><span class="sxs-lookup"><span data-stu-id="ee4f8-103">Revokes an access to a snapshot.</span></span>

## <span data-ttu-id="ee4f8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ee4f8-104">SYNTAX</span></span>

```
Revoke-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee4f8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee4f8-105">DESCRIPTION</span></span>
<span data-ttu-id="ee4f8-106">Командлет **REVOKE-AzSnapshotAccess** отменяет доступ к моментальному снимку.</span><span class="sxs-lookup"><span data-stu-id="ee4f8-106">The **Revoke-AzSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="ee4f8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ee4f8-107">EXAMPLES</span></span>

### <span data-ttu-id="ee4f8-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ee4f8-108">Example 1</span></span>
```
PS C:\> Revoke-AzSnapshotAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="ee4f8-109">Отмена доступа к моментальному снимку с именем "Snapshot01" в группе ресурсов с именем "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="ee4f8-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="ee4f8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ee4f8-110">PARAMETERS</span></span>

### <span data-ttu-id="ee4f8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ee4f8-111">-AsJob</span></span>
<span data-ttu-id="ee4f8-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ee4f8-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ee4f8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee4f8-113">-DefaultProfile</span></span>
<span data-ttu-id="ee4f8-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ee4f8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee4f8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee4f8-115">-ResourceGroupName</span></span>
<span data-ttu-id="ee4f8-116">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ee4f8-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ee4f8-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="ee4f8-117">-SnapshotName</span></span>
<span data-ttu-id="ee4f8-118">Указывает имя снимка.</span><span class="sxs-lookup"><span data-stu-id="ee4f8-118">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="ee4f8-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee4f8-119">-Confirm</span></span>
<span data-ttu-id="ee4f8-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ee4f8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee4f8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee4f8-121">-WhatIf</span></span>
<span data-ttu-id="ee4f8-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ee4f8-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ee4f8-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ee4f8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee4f8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee4f8-124">CommonParameters</span></span>
<span data-ttu-id="ee4f8-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ee4f8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee4f8-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ee4f8-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee4f8-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ee4f8-127">INPUTS</span></span>

### <span data-ttu-id="ee4f8-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ee4f8-128">System.String</span></span>

## <span data-ttu-id="ee4f8-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee4f8-129">OUTPUTS</span></span>

### <span data-ttu-id="ee4f8-130">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="ee4f8-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="ee4f8-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="ee4f8-131">NOTES</span></span>

## <span data-ttu-id="ee4f8-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ee4f8-132">RELATED LINKS</span></span>
