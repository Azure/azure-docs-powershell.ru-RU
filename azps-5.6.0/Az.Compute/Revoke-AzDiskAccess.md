---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/revoke-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzDiskAccess.md
ms.openlocfilehash: 767104edb73265f472e155e8d003b0b5e96906e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963224"
---
# <span data-ttu-id="8b58e-101">Revoke-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="8b58e-101">Revoke-AzDiskAccess</span></span>

## <span data-ttu-id="8b58e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b58e-102">SYNOPSIS</span></span>
<span data-ttu-id="8b58e-103">Отзыв доступа к диску.</span><span class="sxs-lookup"><span data-stu-id="8b58e-103">Revokes an access to a disk.</span></span>

## <span data-ttu-id="8b58e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8b58e-104">SYNTAX</span></span>

```
Revoke-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b58e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b58e-105">DESCRIPTION</span></span>
<span data-ttu-id="8b58e-106">**Cmdlet Revoke-AzDiskAccess** отменяет доступ к диску.</span><span class="sxs-lookup"><span data-stu-id="8b58e-106">The **Revoke-AzDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="8b58e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8b58e-107">EXAMPLES</span></span>

### <span data-ttu-id="8b58e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8b58e-108">Example 1</span></span>
```
PS C:\> Revoke-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="8b58e-109">Ото всем доступ к диску "Диск01" в группе ресурсов "Группа ресурсов01"</span><span class="sxs-lookup"><span data-stu-id="8b58e-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="8b58e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b58e-110">PARAMETERS</span></span>

### <span data-ttu-id="8b58e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b58e-111">-AsJob</span></span>
<span data-ttu-id="8b58e-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8b58e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8b58e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b58e-113">-DefaultProfile</span></span>
<span data-ttu-id="8b58e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8b58e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b58e-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="8b58e-115">-DiskName</span></span>
<span data-ttu-id="8b58e-116">Указывает имя диска.</span><span class="sxs-lookup"><span data-stu-id="8b58e-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="8b58e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b58e-117">-ResourceGroupName</span></span>
<span data-ttu-id="8b58e-118">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8b58e-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8b58e-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8b58e-119">-Confirm</span></span>
<span data-ttu-id="8b58e-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b58e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b58e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b58e-121">-WhatIf</span></span>
<span data-ttu-id="8b58e-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b58e-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8b58e-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8b58e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b58e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b58e-124">CommonParameters</span></span>
<span data-ttu-id="8b58e-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b58e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b58e-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8b58e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b58e-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8b58e-127">INPUTS</span></span>

### <span data-ttu-id="8b58e-128">System.String</span><span class="sxs-lookup"><span data-stu-id="8b58e-128">System.String</span></span>

## <span data-ttu-id="8b58e-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8b58e-129">OUTPUTS</span></span>

### <span data-ttu-id="8b58e-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="8b58e-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="8b58e-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8b58e-131">NOTES</span></span>

## <span data-ttu-id="8b58e-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8b58e-132">RELATED LINKS</span></span>
