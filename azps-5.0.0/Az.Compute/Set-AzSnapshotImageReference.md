---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
ms.openlocfilehash: deb122735b94ed8ac0de63330a9fbdb3ecac81d4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247497"
---
# <span data-ttu-id="8a665-101">Set-AzSnapshotImageReference</span><span class="sxs-lookup"><span data-stu-id="8a665-101">Set-AzSnapshotImageReference</span></span>

## <span data-ttu-id="8a665-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8a665-102">SYNOPSIS</span></span>
<span data-ttu-id="8a665-103">Задает свойства ссылки на изображение для объекта-снимка.</span><span class="sxs-lookup"><span data-stu-id="8a665-103">Sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="8a665-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8a665-104">SYNTAX</span></span>

```
Set-AzSnapshotImageReference [-Snapshot] <PSSnapshot> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a665-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a665-105">DESCRIPTION</span></span>
<span data-ttu-id="8a665-106">Командлет **Set-AzSnapshotImageReference** задает свойства ссылок на изображения в объекте snapshot.</span><span class="sxs-lookup"><span data-stu-id="8a665-106">The **Set-AzSnapshotImageReference** cmdlet sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="8a665-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8a665-107">EXAMPLES</span></span>

### <span data-ttu-id="8a665-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8a665-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotconfig = Set-AzSnapshotImageReference -Snapshot $snapshotconfig -Id $image -Lun 0;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="8a665-109">В первой команде создается локальный объект Snapshot с размером 10 ГБ в Premium_LRS типе учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="8a665-109">The first command creates a local snapshot object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="8a665-110">Она также задает тип операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="8a665-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="8a665-111">Вторая команда задает идентификатор изображения и логический номер устройства 0 для объекта snapshot.</span><span class="sxs-lookup"><span data-stu-id="8a665-111">The second command sets the image ID and the logical unit number 0 for the snapshot object.</span></span>
<span data-ttu-id="8a665-112">Последняя команда принимает объект snapshot и создает моментальный снимок с именем "Snapshot01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="8a665-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="8a665-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8a665-113">PARAMETERS</span></span>

### <span data-ttu-id="8a665-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a665-114">-DefaultProfile</span></span>
<span data-ttu-id="8a665-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8a665-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a665-116">-ID</span><span class="sxs-lookup"><span data-stu-id="8a665-116">-Id</span></span>
<span data-ttu-id="8a665-117">Указывает идентификатор.</span><span class="sxs-lookup"><span data-stu-id="8a665-117">Specifies the ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a665-118">-LUN</span><span class="sxs-lookup"><span data-stu-id="8a665-118">-Lun</span></span>
<span data-ttu-id="8a665-119">Задает логический номер устройства (LUN).</span><span class="sxs-lookup"><span data-stu-id="8a665-119">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a665-120">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="8a665-120">-Snapshot</span></span>
<span data-ttu-id="8a665-121">Указывает локальный объект снимка.</span><span class="sxs-lookup"><span data-stu-id="8a665-121">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a665-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8a665-122">-Confirm</span></span>
<span data-ttu-id="8a665-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8a665-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a665-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a665-124">-WhatIf</span></span>
<span data-ttu-id="8a665-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8a665-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8a665-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8a665-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a665-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a665-127">CommonParameters</span></span>
<span data-ttu-id="8a665-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8a665-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a665-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a665-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a665-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8a665-130">INPUTS</span></span>

### <span data-ttu-id="8a665-131">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="8a665-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="8a665-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8a665-132">System.String</span></span>

### <span data-ttu-id="8a665-133">System. Int32</span><span class="sxs-lookup"><span data-stu-id="8a665-133">System.Int32</span></span>

## <span data-ttu-id="8a665-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a665-134">OUTPUTS</span></span>

### <span data-ttu-id="8a665-135">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="8a665-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="8a665-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="8a665-136">NOTES</span></span>

## <span data-ttu-id="8a665-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8a665-137">RELATED LINKS</span></span>
