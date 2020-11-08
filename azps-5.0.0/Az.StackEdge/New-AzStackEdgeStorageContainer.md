---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageContainer.md
ms.openlocfilehash: 5c0af3ed67bd7cba3408b6628de70c7064120954
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246514"
---
# <span data-ttu-id="9aa5a-101">New-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9aa5a-101">New-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="9aa5a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9aa5a-102">SYNOPSIS</span></span>
<span data-ttu-id="9aa5a-103">Создает новый контейнер хранилища в учетной записи хранилища EDGE на устройстве.</span><span class="sxs-lookup"><span data-stu-id="9aa5a-103">Creates a new storage container in the Edge Storage account on the device.</span></span>

## <span data-ttu-id="9aa5a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9aa5a-104">SYNTAX</span></span>

```
New-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-DataFormat <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9aa5a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9aa5a-105">DESCRIPTION</span></span>
<span data-ttu-id="9aa5a-106">Командлет **New-AzStackEdgeStorageContainer** создает новый контейнер хранилища в учетной записи хранилища EDGE на пограничном устройстве стопки.</span><span class="sxs-lookup"><span data-stu-id="9aa5a-106">The **New-AzStackEdgeStorageContainer** cmdlet creates a new storage container in the Edge Storage account on a Stack Edge device.</span></span>

## <span data-ttu-id="9aa5a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9aa5a-107">EXAMPLES</span></span>

### <span data-ttu-id="9aa5a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9aa5a-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name edgecontainer1 -DataFormat BlockBlob
Name       DataFormat EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ---------------------- ---------- -----------------
container1 BlockBlob  edgestorageaccount1    db-edge    resourceGroupName
```

## <span data-ttu-id="9aa5a-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9aa5a-109">PARAMETERS</span></span>

### <span data-ttu-id="9aa5a-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9aa5a-110">-AsJob</span></span>
<span data-ttu-id="9aa5a-111">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9aa5a-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9aa5a-112">-Формат.</span><span class="sxs-lookup"><span data-stu-id="9aa5a-112">-DataFormat</span></span>
<span data-ttu-id="9aa5a-113">Настройка формата данных ex: PageBlob, BlobBlob</span><span class="sxs-lookup"><span data-stu-id="9aa5a-113">Set Data Format ex: PageBlob, BlobBlob</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9aa5a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9aa5a-114">-DefaultProfile</span></span>
<span data-ttu-id="9aa5a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9aa5a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9aa5a-116">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="9aa5a-116">-DeviceName</span></span>
<span data-ttu-id="9aa5a-117">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="9aa5a-117">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9aa5a-118">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9aa5a-118">-EdgeStorageAccountName</span></span>
<span data-ttu-id="9aa5a-119">Укажите имя существующего EdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9aa5a-119">Provide existing EdgeStorageAccount's Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9aa5a-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9aa5a-120">-Name</span></span>
<span data-ttu-id="9aa5a-121">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="9aa5a-121">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EdgeContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9aa5a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9aa5a-122">-ResourceGroupName</span></span>
<span data-ttu-id="9aa5a-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="9aa5a-123">Resource Group Name</span></span>

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

### <span data-ttu-id="9aa5a-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9aa5a-124">-Confirm</span></span>
<span data-ttu-id="9aa5a-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9aa5a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9aa5a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9aa5a-126">-WhatIf</span></span>
<span data-ttu-id="9aa5a-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9aa5a-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9aa5a-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9aa5a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9aa5a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9aa5a-129">CommonParameters</span></span>
<span data-ttu-id="9aa5a-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9aa5a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9aa5a-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9aa5a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9aa5a-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9aa5a-132">INPUTS</span></span>

### <span data-ttu-id="9aa5a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="9aa5a-133">System.String</span></span>

## <span data-ttu-id="9aa5a-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9aa5a-134">OUTPUTS</span></span>

### <span data-ttu-id="9aa5a-135">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9aa5a-135">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="9aa5a-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="9aa5a-136">NOTES</span></span>

## <span data-ttu-id="9aa5a-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9aa5a-137">RELATED LINKS</span></span>
