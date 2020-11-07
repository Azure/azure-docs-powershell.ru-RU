---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/revoke-azurermdiskaccess
schema: 2.0.0
ms.openlocfilehash: f8da805a2c15356a4bf2188238b9a42a10617427
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913668"
---
# <span data-ttu-id="7a34c-101">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="7a34c-101">Revoke-AzureRmDiskAccess</span></span>

## <span data-ttu-id="7a34c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7a34c-102">SYNOPSIS</span></span>
<span data-ttu-id="7a34c-103">Отменяет доступ к диску.</span><span class="sxs-lookup"><span data-stu-id="7a34c-103">Revokes an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a34c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7a34c-104">SYNTAX</span></span>

```
Revoke-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a34c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a34c-105">DESCRIPTION</span></span>
<span data-ttu-id="7a34c-106">Командлет **REVOKE-AzureRmDiskAccess** отменяет доступ к диску.</span><span class="sxs-lookup"><span data-stu-id="7a34c-106">The **Revoke-AzureRmDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="7a34c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7a34c-107">EXAMPLES</span></span>

### <span data-ttu-id="7a34c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7a34c-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="7a34c-109">Отмена доступа к диску с именем "Disk01" в группе ресурсов с именем "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="7a34c-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="7a34c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7a34c-110">PARAMETERS</span></span>

### <span data-ttu-id="7a34c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a34c-111">-AsJob</span></span>
<span data-ttu-id="7a34c-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7a34c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7a34c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a34c-113">-DefaultProfile</span></span>
<span data-ttu-id="7a34c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7a34c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a34c-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="7a34c-115">-DiskName</span></span>
<span data-ttu-id="7a34c-116">Указывает имя диска.</span><span class="sxs-lookup"><span data-stu-id="7a34c-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="7a34c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a34c-117">-ResourceGroupName</span></span>
<span data-ttu-id="7a34c-118">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7a34c-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="7a34c-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a34c-119">-Confirm</span></span>
<span data-ttu-id="7a34c-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7a34c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a34c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a34c-121">-WhatIf</span></span>
<span data-ttu-id="7a34c-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7a34c-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7a34c-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7a34c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a34c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a34c-124">CommonParameters</span></span>
<span data-ttu-id="7a34c-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7a34c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a34c-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a34c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a34c-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7a34c-127">INPUTS</span></span>

### <span data-ttu-id="7a34c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7a34c-128">System.String</span></span>

## <span data-ttu-id="7a34c-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a34c-129">OUTPUTS</span></span>

### <span data-ttu-id="7a34c-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="7a34c-130">System.Object</span></span>

## <span data-ttu-id="7a34c-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="7a34c-131">NOTES</span></span>

## <span data-ttu-id="7a34c-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7a34c-132">RELATED LINKS</span></span>

