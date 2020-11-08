---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/revoke-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzDiskAccess.md
ms.openlocfilehash: 76fb2e7483bb510d5eceb92b51f7e5e538c3b22b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245604"
---
# <span data-ttu-id="d315d-101">Revoke-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="d315d-101">Revoke-AzDiskAccess</span></span>

## <span data-ttu-id="d315d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d315d-102">SYNOPSIS</span></span>
<span data-ttu-id="d315d-103">Отменяет доступ к диску.</span><span class="sxs-lookup"><span data-stu-id="d315d-103">Revokes an access to a disk.</span></span>

## <span data-ttu-id="d315d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d315d-104">SYNTAX</span></span>

```
Revoke-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d315d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d315d-105">DESCRIPTION</span></span>
<span data-ttu-id="d315d-106">Командлет **REVOKE-AzDiskAccess** отменяет доступ к диску.</span><span class="sxs-lookup"><span data-stu-id="d315d-106">The **Revoke-AzDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="d315d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d315d-107">EXAMPLES</span></span>

### <span data-ttu-id="d315d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d315d-108">Example 1</span></span>
```
PS C:\> Revoke-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="d315d-109">Отмена доступа к диску с именем "Disk01" в группе ресурсов с именем "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="d315d-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="d315d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d315d-110">PARAMETERS</span></span>

### <span data-ttu-id="d315d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d315d-111">-AsJob</span></span>
<span data-ttu-id="d315d-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d315d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d315d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d315d-113">-DefaultProfile</span></span>
<span data-ttu-id="d315d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d315d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d315d-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="d315d-115">-DiskName</span></span>
<span data-ttu-id="d315d-116">Указывает имя диска.</span><span class="sxs-lookup"><span data-stu-id="d315d-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="d315d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d315d-117">-ResourceGroupName</span></span>
<span data-ttu-id="d315d-118">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d315d-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d315d-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d315d-119">-Confirm</span></span>
<span data-ttu-id="d315d-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d315d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d315d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d315d-121">-WhatIf</span></span>
<span data-ttu-id="d315d-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d315d-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d315d-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d315d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d315d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d315d-124">CommonParameters</span></span>
<span data-ttu-id="d315d-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d315d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d315d-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d315d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d315d-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d315d-127">INPUTS</span></span>

### <span data-ttu-id="d315d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d315d-128">System.String</span></span>

## <span data-ttu-id="d315d-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d315d-129">OUTPUTS</span></span>

### <span data-ttu-id="d315d-130">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="d315d-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="d315d-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="d315d-131">NOTES</span></span>

## <span data-ttu-id="d315d-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d315d-132">RELATED LINKS</span></span>
