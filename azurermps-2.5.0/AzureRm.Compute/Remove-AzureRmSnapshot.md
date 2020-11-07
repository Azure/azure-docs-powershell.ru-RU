---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermsnapshot
schema: 2.0.0
ms.openlocfilehash: cf63923b278f009cb676c79642882e64e6b8e303
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914530"
---
# <span data-ttu-id="1f174-101">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="1f174-101">Remove-AzureRmSnapshot</span></span>

## <span data-ttu-id="1f174-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1f174-102">SYNOPSIS</span></span>
<span data-ttu-id="1f174-103">Удаляет снимок.</span><span class="sxs-lookup"><span data-stu-id="1f174-103">Removes a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f174-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1f174-104">SYNTAX</span></span>

```
Remove-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f174-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f174-105">DESCRIPTION</span></span>
<span data-ttu-id="1f174-106">Командлет **Remove-AzureRmSnapshot** удаляет моментальный снимок.</span><span class="sxs-lookup"><span data-stu-id="1f174-106">The **Remove-AzureRmSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="1f174-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1f174-107">EXAMPLES</span></span>

### <span data-ttu-id="1f174-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1f174-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="1f174-109">Эта команда удаляет моментальный снимок с именем "Snapshot01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="1f174-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="1f174-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1f174-110">PARAMETERS</span></span>

### <span data-ttu-id="1f174-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f174-111">-AsJob</span></span>
<span data-ttu-id="1f174-112">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="1f174-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="1f174-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f174-113">-DefaultProfile</span></span>
<span data-ttu-id="1f174-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1f174-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f174-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1f174-115">-Force</span></span>
<span data-ttu-id="1f174-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="1f174-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1f174-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f174-117">-ResourceGroupName</span></span>
<span data-ttu-id="1f174-118">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1f174-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1f174-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="1f174-119">-SnapshotName</span></span>
<span data-ttu-id="1f174-120">Указывает имя снимка.</span><span class="sxs-lookup"><span data-stu-id="1f174-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="1f174-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f174-121">-Confirm</span></span>
<span data-ttu-id="1f174-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1f174-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f174-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f174-123">-WhatIf</span></span>
<span data-ttu-id="1f174-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1f174-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f174-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1f174-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f174-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f174-126">CommonParameters</span></span>
<span data-ttu-id="1f174-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1f174-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f174-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f174-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f174-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1f174-129">INPUTS</span></span>

### <span data-ttu-id="1f174-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1f174-130">System.String</span></span>

## <span data-ttu-id="1f174-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f174-131">OUTPUTS</span></span>

### <span data-ttu-id="1f174-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="1f174-132">System.Object</span></span>

## <span data-ttu-id="1f174-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="1f174-133">NOTES</span></span>

## <span data-ttu-id="1f174-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1f174-134">RELATED LINKS</span></span>

