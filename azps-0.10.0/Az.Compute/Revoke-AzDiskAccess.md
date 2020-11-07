---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/revoke-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Revoke-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Revoke-AzDiskAccess.md
ms.openlocfilehash: 67c96d257be803e77555a7a93d8f9b1ebbbbf8c2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911389"
---
# <span data-ttu-id="11b4e-101">Revoke-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="11b4e-101">Revoke-AzDiskAccess</span></span>

## <span data-ttu-id="11b4e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="11b4e-102">SYNOPSIS</span></span>
<span data-ttu-id="11b4e-103">Отменяет доступ к диску.</span><span class="sxs-lookup"><span data-stu-id="11b4e-103">Revokes an access to a disk.</span></span>

## <span data-ttu-id="11b4e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="11b4e-104">SYNTAX</span></span>

```
Revoke-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11b4e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="11b4e-105">DESCRIPTION</span></span>
<span data-ttu-id="11b4e-106">Командлет **REVOKE-AzDiskAccess** отменяет доступ к диску.</span><span class="sxs-lookup"><span data-stu-id="11b4e-106">The **Revoke-AzDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="11b4e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="11b4e-107">EXAMPLES</span></span>

### <span data-ttu-id="11b4e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="11b4e-108">Example 1</span></span>
```
PS C:\> Revoke-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="11b4e-109">Отмена доступа к диску с именем "Disk01" в группе ресурсов с именем "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="11b4e-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="11b4e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="11b4e-110">PARAMETERS</span></span>

### <span data-ttu-id="11b4e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11b4e-111">-AsJob</span></span>
<span data-ttu-id="11b4e-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="11b4e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="11b4e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11b4e-113">-DefaultProfile</span></span>
<span data-ttu-id="11b4e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="11b4e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11b4e-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="11b4e-115">-DiskName</span></span>
<span data-ttu-id="11b4e-116">Указывает имя диска.</span><span class="sxs-lookup"><span data-stu-id="11b4e-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="11b4e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11b4e-117">-ResourceGroupName</span></span>
<span data-ttu-id="11b4e-118">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="11b4e-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="11b4e-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11b4e-119">-Confirm</span></span>
<span data-ttu-id="11b4e-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="11b4e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11b4e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11b4e-121">-WhatIf</span></span>
<span data-ttu-id="11b4e-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="11b4e-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="11b4e-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="11b4e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11b4e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11b4e-124">CommonParameters</span></span>
<span data-ttu-id="11b4e-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="11b4e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11b4e-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11b4e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11b4e-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="11b4e-127">INPUTS</span></span>

### <span data-ttu-id="11b4e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="11b4e-128">System.String</span></span>

## <span data-ttu-id="11b4e-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="11b4e-129">OUTPUTS</span></span>

### <span data-ttu-id="11b4e-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="11b4e-130">System.Object</span></span>

## <span data-ttu-id="11b4e-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="11b4e-131">NOTES</span></span>

## <span data-ttu-id="11b4e-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="11b4e-132">RELATED LINKS</span></span>

