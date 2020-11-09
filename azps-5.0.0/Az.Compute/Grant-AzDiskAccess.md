---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/grant-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzDiskAccess.md
ms.openlocfilehash: 39565aa0675a0afc5f6f3996cad522b435a1a9b2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246808"
---
# <span data-ttu-id="4bc08-101">Grant-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="4bc08-101">Grant-AzDiskAccess</span></span>

## <span data-ttu-id="4bc08-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4bc08-102">SYNOPSIS</span></span>
<span data-ttu-id="4bc08-103">Предоставление доступа к диску.</span><span class="sxs-lookup"><span data-stu-id="4bc08-103">Grants an access to a disk.</span></span>

## <span data-ttu-id="4bc08-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4bc08-104">SYNTAX</span></span>

```
Grant-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4bc08-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4bc08-105">DESCRIPTION</span></span>
<span data-ttu-id="4bc08-106">Командлет **Grant-AzDiskAccess** предоставляет доступ к диску.</span><span class="sxs-lookup"><span data-stu-id="4bc08-106">The **Grant-AzDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="4bc08-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4bc08-107">EXAMPLES</span></span>

### <span data-ttu-id="4bc08-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4bc08-108">Example 1</span></span>
```
PS C:\> Grant-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="4bc08-109">Предоставление доступа для чтения к диску с именем "Disk01" в группе ресурсов с именем "ResourceGroup01" для 60 секунд.</span><span class="sxs-lookup"><span data-stu-id="4bc08-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="4bc08-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4bc08-110">PARAMETERS</span></span>

### <span data-ttu-id="4bc08-111">-Доступ</span><span class="sxs-lookup"><span data-stu-id="4bc08-111">-Access</span></span>
<span data-ttu-id="4bc08-112">Определяет уровень доступа.</span><span class="sxs-lookup"><span data-stu-id="4bc08-112">Specifies Access level.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bc08-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4bc08-113">-AsJob</span></span>
<span data-ttu-id="4bc08-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="4bc08-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4bc08-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bc08-115">-DefaultProfile</span></span>
<span data-ttu-id="4bc08-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4bc08-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4bc08-117">-DiskName</span><span class="sxs-lookup"><span data-stu-id="4bc08-117">-DiskName</span></span>
<span data-ttu-id="4bc08-118">Указывает имя диска.</span><span class="sxs-lookup"><span data-stu-id="4bc08-118">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="4bc08-119">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="4bc08-119">-DurationInSecond</span></span>
<span data-ttu-id="4bc08-120">Указывает продолжительность доступа в секундах.</span><span class="sxs-lookup"><span data-stu-id="4bc08-120">Specifies access duration in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bc08-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bc08-121">-ResourceGroupName</span></span>
<span data-ttu-id="4bc08-122">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4bc08-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4bc08-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4bc08-123">-Confirm</span></span>
<span data-ttu-id="4bc08-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4bc08-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bc08-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bc08-125">-WhatIf</span></span>
<span data-ttu-id="4bc08-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4bc08-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4bc08-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4bc08-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bc08-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bc08-128">CommonParameters</span></span>
<span data-ttu-id="4bc08-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4bc08-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bc08-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4bc08-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bc08-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4bc08-131">INPUTS</span></span>

### <span data-ttu-id="4bc08-132">System. String</span><span class="sxs-lookup"><span data-stu-id="4bc08-132">System.String</span></span>

## <span data-ttu-id="4bc08-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4bc08-133">OUTPUTS</span></span>

### <span data-ttu-id="4bc08-134">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSAccessUri</span><span class="sxs-lookup"><span data-stu-id="4bc08-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="4bc08-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="4bc08-135">NOTES</span></span>

## <span data-ttu-id="4bc08-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4bc08-136">RELATED LINKS</span></span>