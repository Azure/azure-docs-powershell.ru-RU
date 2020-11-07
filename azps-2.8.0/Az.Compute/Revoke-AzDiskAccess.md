---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/revoke-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzDiskAccess.md
ms.openlocfilehash: 13ae9cc51b5a1f29b995e9dd5c98ee1243339585
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721734"
---
# <span data-ttu-id="43625-101">Revoke-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="43625-101">Revoke-AzDiskAccess</span></span>

## <span data-ttu-id="43625-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="43625-102">SYNOPSIS</span></span>
<span data-ttu-id="43625-103">Отменяет доступ к диску.</span><span class="sxs-lookup"><span data-stu-id="43625-103">Revokes an access to a disk.</span></span>

## <span data-ttu-id="43625-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="43625-104">SYNTAX</span></span>

```
Revoke-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43625-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="43625-105">DESCRIPTION</span></span>
<span data-ttu-id="43625-106">Командлет **REVOKE-AzDiskAccess** отменяет доступ к диску.</span><span class="sxs-lookup"><span data-stu-id="43625-106">The **Revoke-AzDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="43625-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="43625-107">EXAMPLES</span></span>

### <span data-ttu-id="43625-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="43625-108">Example 1</span></span>
```
PS C:\> Revoke-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="43625-109">Отмена доступа к диску с именем "Disk01" в группе ресурсов с именем "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="43625-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="43625-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="43625-110">PARAMETERS</span></span>

### <span data-ttu-id="43625-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43625-111">-AsJob</span></span>
<span data-ttu-id="43625-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="43625-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="43625-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43625-113">-DefaultProfile</span></span>
<span data-ttu-id="43625-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="43625-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43625-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="43625-115">-DiskName</span></span>
<span data-ttu-id="43625-116">Указывает имя диска.</span><span class="sxs-lookup"><span data-stu-id="43625-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="43625-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43625-117">-ResourceGroupName</span></span>
<span data-ttu-id="43625-118">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="43625-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="43625-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43625-119">-Confirm</span></span>
<span data-ttu-id="43625-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="43625-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43625-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43625-121">-WhatIf</span></span>
<span data-ttu-id="43625-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="43625-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="43625-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="43625-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43625-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43625-124">CommonParameters</span></span>
<span data-ttu-id="43625-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="43625-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43625-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43625-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43625-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="43625-127">INPUTS</span></span>

### <span data-ttu-id="43625-128">System. String</span><span class="sxs-lookup"><span data-stu-id="43625-128">System.String</span></span>

## <span data-ttu-id="43625-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="43625-129">OUTPUTS</span></span>

### <span data-ttu-id="43625-130">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="43625-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="43625-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="43625-131">NOTES</span></span>

## <span data-ttu-id="43625-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="43625-132">RELATED LINKS</span></span>
