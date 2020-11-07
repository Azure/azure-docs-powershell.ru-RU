---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/grant-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
ms.openlocfilehash: e4283b23fb4a82c17f35354d854c30c3ec1b2329
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911487"
---
# <span data-ttu-id="72e55-101">Grant-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="72e55-101">Grant-AzSnapshotAccess</span></span>

## <span data-ttu-id="72e55-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="72e55-102">SYNOPSIS</span></span>
<span data-ttu-id="72e55-103">Предоставляет доступ к снимку.</span><span class="sxs-lookup"><span data-stu-id="72e55-103">Grants an access to a snapshot.</span></span>

## <span data-ttu-id="72e55-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="72e55-104">SYNTAX</span></span>

```
Grant-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-Access] <AccessLevel>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="72e55-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="72e55-105">DESCRIPTION</span></span>
<span data-ttu-id="72e55-106">Командлет **Grant-AzSnapshotAccess** предоставляет доступ к снимку.</span><span class="sxs-lookup"><span data-stu-id="72e55-106">The **Grant-AzSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="72e55-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="72e55-107">EXAMPLES</span></span>

### <span data-ttu-id="72e55-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="72e55-108">Example 1</span></span>
```
PS C:\> Grant-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="72e55-109">Предоставьте доступ на чтение к снимку с именем Snapshot01 в группе ресурсов с именем "ResourceGroup01" для 60 секунд.</span><span class="sxs-lookup"><span data-stu-id="72e55-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="72e55-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="72e55-110">PARAMETERS</span></span>

### <span data-ttu-id="72e55-111">-Доступ</span><span class="sxs-lookup"><span data-stu-id="72e55-111">-Access</span></span>
<span data-ttu-id="72e55-112">Определяет уровень доступа.</span><span class="sxs-lookup"><span data-stu-id="72e55-112">Specifies Access level.</span></span>

```yaml
Type: AccessLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72e55-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="72e55-113">-AsJob</span></span>
<span data-ttu-id="72e55-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="72e55-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72e55-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72e55-115">-DefaultProfile</span></span>
<span data-ttu-id="72e55-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="72e55-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72e55-117">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="72e55-117">-DurationInSecond</span></span>
<span data-ttu-id="72e55-118">Указывает продолжительность доступа в секундах.</span><span class="sxs-lookup"><span data-stu-id="72e55-118">Specifies access duration in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72e55-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72e55-119">-ResourceGroupName</span></span>
<span data-ttu-id="72e55-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="72e55-120">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72e55-121">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="72e55-121">-SnapshotName</span></span>
<span data-ttu-id="72e55-122">Указывает имя снимка.</span><span class="sxs-lookup"><span data-stu-id="72e55-122">Specifies the name of a snapshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72e55-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="72e55-123">-Confirm</span></span>
<span data-ttu-id="72e55-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="72e55-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72e55-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72e55-125">-WhatIf</span></span>
<span data-ttu-id="72e55-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="72e55-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="72e55-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="72e55-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72e55-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72e55-128">CommonParameters</span></span>
<span data-ttu-id="72e55-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="72e55-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72e55-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72e55-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72e55-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="72e55-131">INPUTS</span></span>

### <span data-ttu-id="72e55-132">System. String</span><span class="sxs-lookup"><span data-stu-id="72e55-132">System.String</span></span>

## <span data-ttu-id="72e55-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="72e55-133">OUTPUTS</span></span>

### <span data-ttu-id="72e55-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="72e55-134">System.Object</span></span>

## <span data-ttu-id="72e55-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="72e55-135">NOTES</span></span>

## <span data-ttu-id="72e55-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="72e55-136">RELATED LINKS</span></span>

