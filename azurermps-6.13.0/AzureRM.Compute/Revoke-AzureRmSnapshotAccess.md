---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/revoke-azurermsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Revoke-AzureRmSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Revoke-AzureRmSnapshotAccess.md
ms.openlocfilehash: eb71d1a74e68bdf4157cacd4b87aa9a05bdc00db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556771"
---
# <span data-ttu-id="1267b-101">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="1267b-101">Revoke-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="1267b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1267b-102">SYNOPSIS</span></span>
<span data-ttu-id="1267b-103">Отменяет доступ к снимку.</span><span class="sxs-lookup"><span data-stu-id="1267b-103">Revokes an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1267b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1267b-104">SYNTAX</span></span>

```
Revoke-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1267b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1267b-105">DESCRIPTION</span></span>
<span data-ttu-id="1267b-106">Командлет **REVOKE-AzureRmSnapshotAccess** отменяет доступ к моментальному снимку.</span><span class="sxs-lookup"><span data-stu-id="1267b-106">The **Revoke-AzureRmSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="1267b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1267b-107">EXAMPLES</span></span>

### <span data-ttu-id="1267b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1267b-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="1267b-109">Отмена доступа к моментальному снимку с именем "Snapshot01" в группе ресурсов с именем "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="1267b-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="1267b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1267b-110">PARAMETERS</span></span>

### <span data-ttu-id="1267b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1267b-111">-AsJob</span></span>
<span data-ttu-id="1267b-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="1267b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1267b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1267b-113">-DefaultProfile</span></span>
<span data-ttu-id="1267b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1267b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1267b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1267b-115">-ResourceGroupName</span></span>
<span data-ttu-id="1267b-116">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1267b-116">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1267b-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="1267b-117">-SnapshotName</span></span>
<span data-ttu-id="1267b-118">Указывает имя снимка.</span><span class="sxs-lookup"><span data-stu-id="1267b-118">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1267b-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1267b-119">-Confirm</span></span>
<span data-ttu-id="1267b-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1267b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1267b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1267b-121">-WhatIf</span></span>
<span data-ttu-id="1267b-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1267b-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1267b-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1267b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1267b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1267b-124">CommonParameters</span></span>
<span data-ttu-id="1267b-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1267b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1267b-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1267b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1267b-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1267b-127">INPUTS</span></span>

### <span data-ttu-id="1267b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="1267b-128">System.String</span></span>

## <span data-ttu-id="1267b-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1267b-129">OUTPUTS</span></span>

### <span data-ttu-id="1267b-130">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="1267b-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="1267b-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="1267b-131">NOTES</span></span>

## <span data-ttu-id="1267b-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1267b-132">RELATED LINKS</span></span>
