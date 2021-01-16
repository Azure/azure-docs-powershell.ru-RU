---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/grant-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzDiskAccess.md
ms.openlocfilehash: 39565aa0675a0afc5f6f3996cad522b435a1a9b2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394004"
---
# <span data-ttu-id="eb5ae-101">Grant-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="eb5ae-101">Grant-AzDiskAccess</span></span>

## <span data-ttu-id="eb5ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb5ae-102">SYNOPSIS</span></span>
<span data-ttu-id="eb5ae-103">Предоставляет доступ к диску.</span><span class="sxs-lookup"><span data-stu-id="eb5ae-103">Grants an access to a disk.</span></span>

## <span data-ttu-id="eb5ae-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="eb5ae-104">SYNTAX</span></span>

```
Grant-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eb5ae-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb5ae-105">DESCRIPTION</span></span>
<span data-ttu-id="eb5ae-106">Для доступа к диску предоставляется cmdlet **Grant-AzDiskAccess.**</span><span class="sxs-lookup"><span data-stu-id="eb5ae-106">The **Grant-AzDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="eb5ae-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="eb5ae-107">EXAMPLES</span></span>

### <span data-ttu-id="eb5ae-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="eb5ae-108">Example 1</span></span>
```
PS C:\> Grant-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="eb5ae-109">Предоставить "Чтение" доступ к диску "Диск01" в группе ресурсов "Группа ресурсов01" на 60 секунд.</span><span class="sxs-lookup"><span data-stu-id="eb5ae-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="eb5ae-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb5ae-110">PARAMETERS</span></span>

### <span data-ttu-id="eb5ae-111">-Access</span><span class="sxs-lookup"><span data-stu-id="eb5ae-111">-Access</span></span>
<span data-ttu-id="eb5ae-112">Определяет уровень доступа.</span><span class="sxs-lookup"><span data-stu-id="eb5ae-112">Specifies Access level.</span></span>

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

### <span data-ttu-id="eb5ae-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eb5ae-113">-AsJob</span></span>
<span data-ttu-id="eb5ae-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="eb5ae-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eb5ae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb5ae-115">-DefaultProfile</span></span>
<span data-ttu-id="eb5ae-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eb5ae-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb5ae-117">-DiskName</span><span class="sxs-lookup"><span data-stu-id="eb5ae-117">-DiskName</span></span>
<span data-ttu-id="eb5ae-118">Указывает имя диска.</span><span class="sxs-lookup"><span data-stu-id="eb5ae-118">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="eb5ae-119">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="eb5ae-119">-DurationInSecond</span></span>
<span data-ttu-id="eb5ae-120">Определяет длительность доступа в секундах.</span><span class="sxs-lookup"><span data-stu-id="eb5ae-120">Specifies access duration in seconds.</span></span>

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

### <span data-ttu-id="eb5ae-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb5ae-121">-ResourceGroupName</span></span>
<span data-ttu-id="eb5ae-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eb5ae-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="eb5ae-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eb5ae-123">-Confirm</span></span>
<span data-ttu-id="eb5ae-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="eb5ae-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb5ae-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb5ae-125">-WhatIf</span></span>
<span data-ttu-id="eb5ae-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb5ae-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eb5ae-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="eb5ae-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb5ae-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb5ae-128">CommonParameters</span></span>
<span data-ttu-id="eb5ae-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb5ae-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb5ae-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eb5ae-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb5ae-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eb5ae-131">INPUTS</span></span>

### <span data-ttu-id="eb5ae-132">System.String</span><span class="sxs-lookup"><span data-stu-id="eb5ae-132">System.String</span></span>

## <span data-ttu-id="eb5ae-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="eb5ae-133">OUTPUTS</span></span>

### <span data-ttu-id="eb5ae-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span><span class="sxs-lookup"><span data-stu-id="eb5ae-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="eb5ae-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="eb5ae-135">NOTES</span></span>

## <span data-ttu-id="eb5ae-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eb5ae-136">RELATED LINKS</span></span>