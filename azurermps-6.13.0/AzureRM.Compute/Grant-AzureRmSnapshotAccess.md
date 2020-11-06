---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/grant-azurermsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Grant-AzureRmSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Grant-AzureRmSnapshotAccess.md
ms.openlocfilehash: b60abc403beea938e24ffaa59e634a36611d150b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564687"
---
# <span data-ttu-id="7d014-101">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="7d014-101">Grant-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="7d014-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7d014-102">SYNOPSIS</span></span>
<span data-ttu-id="7d014-103">Предоставляет доступ к снимку.</span><span class="sxs-lookup"><span data-stu-id="7d014-103">Grants an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d014-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7d014-104">SYNTAX</span></span>

```
Grant-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7d014-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d014-105">DESCRIPTION</span></span>
<span data-ttu-id="7d014-106">Командлет **Grant-AzureRmSnapshotAccess** предоставляет доступ к снимку.</span><span class="sxs-lookup"><span data-stu-id="7d014-106">The **Grant-AzureRmSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="7d014-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7d014-107">EXAMPLES</span></span>

### <span data-ttu-id="7d014-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7d014-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="7d014-109">Предоставьте доступ на чтение к снимку с именем Snapshot01 в группе ресурсов с именем "ResourceGroup01" для 60 секунд.</span><span class="sxs-lookup"><span data-stu-id="7d014-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="7d014-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7d014-110">PARAMETERS</span></span>

### <span data-ttu-id="7d014-111">-Доступ</span><span class="sxs-lookup"><span data-stu-id="7d014-111">-Access</span></span>
<span data-ttu-id="7d014-112">Определяет уровень доступа.</span><span class="sxs-lookup"><span data-stu-id="7d014-112">Specifies Access level.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d014-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7d014-113">-AsJob</span></span>
<span data-ttu-id="7d014-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7d014-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7d014-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d014-115">-DefaultProfile</span></span>
<span data-ttu-id="7d014-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7d014-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d014-117">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="7d014-117">-DurationInSecond</span></span>
<span data-ttu-id="7d014-118">Указывает продолжительность доступа в секундах.</span><span class="sxs-lookup"><span data-stu-id="7d014-118">Specifies access duration in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d014-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d014-119">-ResourceGroupName</span></span>
<span data-ttu-id="7d014-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7d014-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="7d014-121">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="7d014-121">-SnapshotName</span></span>
<span data-ttu-id="7d014-122">Указывает имя снимка.</span><span class="sxs-lookup"><span data-stu-id="7d014-122">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="7d014-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7d014-123">-Confirm</span></span>
<span data-ttu-id="7d014-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7d014-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d014-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d014-125">-WhatIf</span></span>
<span data-ttu-id="7d014-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7d014-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7d014-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7d014-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d014-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d014-128">CommonParameters</span></span>
<span data-ttu-id="7d014-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7d014-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d014-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d014-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d014-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7d014-131">INPUTS</span></span>

### <span data-ttu-id="7d014-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7d014-132">System.String</span></span>

## <span data-ttu-id="7d014-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d014-133">OUTPUTS</span></span>

### <span data-ttu-id="7d014-134">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSAccessUri</span><span class="sxs-lookup"><span data-stu-id="7d014-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="7d014-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="7d014-135">NOTES</span></span>

## <span data-ttu-id="7d014-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7d014-136">RELATED LINKS</span></span>
