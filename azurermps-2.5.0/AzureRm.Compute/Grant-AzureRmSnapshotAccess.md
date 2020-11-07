---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/grant-azurermsnapshotaccess
schema: 2.0.0
ms.openlocfilehash: b1957543c959a18c9fd0fe4fc12de02064ffdcf0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914230"
---
# <span data-ttu-id="50df9-101">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="50df9-101">Grant-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="50df9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="50df9-102">SYNOPSIS</span></span>
<span data-ttu-id="50df9-103">Предоставляет доступ к снимку.</span><span class="sxs-lookup"><span data-stu-id="50df9-103">Grants an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50df9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="50df9-104">SYNTAX</span></span>

```
Grant-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-Access] <AccessLevel>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="50df9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="50df9-105">DESCRIPTION</span></span>
<span data-ttu-id="50df9-106">Командлет **Grant-AzureRmSnapshotAccess** предоставляет доступ к снимку.</span><span class="sxs-lookup"><span data-stu-id="50df9-106">The **Grant-AzureRmSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="50df9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="50df9-107">EXAMPLES</span></span>

### <span data-ttu-id="50df9-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="50df9-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="50df9-109">Предоставьте доступ на чтение к снимку с именем Snapshot01 в группе ресурсов с именем "ResourceGroup01" для 60 секунд.</span><span class="sxs-lookup"><span data-stu-id="50df9-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="50df9-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="50df9-110">PARAMETERS</span></span>

### <span data-ttu-id="50df9-111">-Доступ</span><span class="sxs-lookup"><span data-stu-id="50df9-111">-Access</span></span>
<span data-ttu-id="50df9-112">Определяет уровень доступа.</span><span class="sxs-lookup"><span data-stu-id="50df9-112">Specifies Access level.</span></span>

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

### <span data-ttu-id="50df9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="50df9-113">-AsJob</span></span>
<span data-ttu-id="50df9-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="50df9-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="50df9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50df9-115">-DefaultProfile</span></span>
<span data-ttu-id="50df9-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="50df9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50df9-117">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="50df9-117">-DurationInSecond</span></span>
<span data-ttu-id="50df9-118">Указывает продолжительность доступа в секундах.</span><span class="sxs-lookup"><span data-stu-id="50df9-118">Specifies access duration in seconds.</span></span>

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

### <span data-ttu-id="50df9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50df9-119">-ResourceGroupName</span></span>
<span data-ttu-id="50df9-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="50df9-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="50df9-121">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="50df9-121">-SnapshotName</span></span>
<span data-ttu-id="50df9-122">Указывает имя снимка.</span><span class="sxs-lookup"><span data-stu-id="50df9-122">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="50df9-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="50df9-123">-Confirm</span></span>
<span data-ttu-id="50df9-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="50df9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50df9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50df9-125">-WhatIf</span></span>
<span data-ttu-id="50df9-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="50df9-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="50df9-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="50df9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50df9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50df9-128">CommonParameters</span></span>
<span data-ttu-id="50df9-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="50df9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50df9-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50df9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50df9-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="50df9-131">INPUTS</span></span>

### <span data-ttu-id="50df9-132">System. String</span><span class="sxs-lookup"><span data-stu-id="50df9-132">System.String</span></span>

## <span data-ttu-id="50df9-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="50df9-133">OUTPUTS</span></span>

### <span data-ttu-id="50df9-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="50df9-134">System.Object</span></span>

## <span data-ttu-id="50df9-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="50df9-135">NOTES</span></span>

## <span data-ttu-id="50df9-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="50df9-136">RELATED LINKS</span></span>

