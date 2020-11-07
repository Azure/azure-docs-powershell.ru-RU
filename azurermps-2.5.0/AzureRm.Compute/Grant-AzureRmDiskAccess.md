---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/grant-azurermdiskaccess
schema: 2.0.0
ms.openlocfilehash: c574b273082d3c7e840d589fe765190d99028d89
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914233"
---
# <span data-ttu-id="59b1c-101">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="59b1c-101">Grant-AzureRmDiskAccess</span></span>

## <span data-ttu-id="59b1c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="59b1c-102">SYNOPSIS</span></span>
<span data-ttu-id="59b1c-103">Предоставление доступа к диску.</span><span class="sxs-lookup"><span data-stu-id="59b1c-103">Grants an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59b1c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="59b1c-104">SYNTAX</span></span>

```
Grant-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-Access] <AccessLevel>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="59b1c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="59b1c-105">DESCRIPTION</span></span>
<span data-ttu-id="59b1c-106">Командлет **Grant-AzureRmDiskAccess** предоставляет доступ к диску.</span><span class="sxs-lookup"><span data-stu-id="59b1c-106">The **Grant-AzureRmDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="59b1c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="59b1c-107">EXAMPLES</span></span>

### <span data-ttu-id="59b1c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="59b1c-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="59b1c-109">Предоставление доступа для чтения к диску с именем "Disk01" в группе ресурсов с именем "ResourceGroup01" для 60 секунд.</span><span class="sxs-lookup"><span data-stu-id="59b1c-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="59b1c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="59b1c-110">PARAMETERS</span></span>

### <span data-ttu-id="59b1c-111">-Доступ</span><span class="sxs-lookup"><span data-stu-id="59b1c-111">-Access</span></span>
<span data-ttu-id="59b1c-112">Определяет уровень доступа.</span><span class="sxs-lookup"><span data-stu-id="59b1c-112">Specifies Access level.</span></span>

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

### <span data-ttu-id="59b1c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="59b1c-113">-AsJob</span></span>
<span data-ttu-id="59b1c-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="59b1c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="59b1c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59b1c-115">-DefaultProfile</span></span>
<span data-ttu-id="59b1c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="59b1c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59b1c-117">-DiskName</span><span class="sxs-lookup"><span data-stu-id="59b1c-117">-DiskName</span></span>
<span data-ttu-id="59b1c-118">Указывает имя диска.</span><span class="sxs-lookup"><span data-stu-id="59b1c-118">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="59b1c-119">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="59b1c-119">-DurationInSecond</span></span>
<span data-ttu-id="59b1c-120">Указывает продолжительность доступа в секундах.</span><span class="sxs-lookup"><span data-stu-id="59b1c-120">Specifies access duration in seconds.</span></span>

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

### <span data-ttu-id="59b1c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59b1c-121">-ResourceGroupName</span></span>
<span data-ttu-id="59b1c-122">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="59b1c-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="59b1c-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="59b1c-123">-Confirm</span></span>
<span data-ttu-id="59b1c-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="59b1c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59b1c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59b1c-125">-WhatIf</span></span>
<span data-ttu-id="59b1c-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="59b1c-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="59b1c-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="59b1c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59b1c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59b1c-128">CommonParameters</span></span>
<span data-ttu-id="59b1c-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="59b1c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59b1c-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59b1c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59b1c-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="59b1c-131">INPUTS</span></span>

### <span data-ttu-id="59b1c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="59b1c-132">System.String</span></span>

## <span data-ttu-id="59b1c-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="59b1c-133">OUTPUTS</span></span>

### <span data-ttu-id="59b1c-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="59b1c-134">System.Object</span></span>

## <span data-ttu-id="59b1c-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="59b1c-135">NOTES</span></span>

## <span data-ttu-id="59b1c-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="59b1c-136">RELATED LINKS</span></span>

