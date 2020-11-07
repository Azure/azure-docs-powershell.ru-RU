---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermdisk
schema: 2.0.0
ms.openlocfilehash: 5987e92e281dd892ebc56c0a18ca59fc99cfc82d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914546"
---
# <span data-ttu-id="227fb-101">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="227fb-101">Remove-AzureRmDisk</span></span>

## <span data-ttu-id="227fb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="227fb-102">SYNOPSIS</span></span>
<span data-ttu-id="227fb-103">Удаление диска.</span><span class="sxs-lookup"><span data-stu-id="227fb-103">Removes a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="227fb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="227fb-104">SYNTAX</span></span>

```
Remove-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="227fb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="227fb-105">DESCRIPTION</span></span>
<span data-ttu-id="227fb-106">Командлет **Remove-AzureRmDisk** удаляет диск.</span><span class="sxs-lookup"><span data-stu-id="227fb-106">The **Remove-AzureRmDisk** cmdlet removes a disk.</span></span>

## <span data-ttu-id="227fb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="227fb-107">EXAMPLES</span></span>

### <span data-ttu-id="227fb-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="227fb-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Force;
```

<span data-ttu-id="227fb-109">Эта команда удаляет диск с именем "Disk01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="227fb-109">This command removes the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="227fb-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="227fb-110">PARAMETERS</span></span>

### <span data-ttu-id="227fb-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="227fb-111">-AsJob</span></span>
<span data-ttu-id="227fb-112">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="227fb-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="227fb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="227fb-113">-DefaultProfile</span></span>
<span data-ttu-id="227fb-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="227fb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="227fb-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="227fb-115">-DiskName</span></span>
<span data-ttu-id="227fb-116">Указывает имя диска.</span><span class="sxs-lookup"><span data-stu-id="227fb-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="227fb-117">-Force</span><span class="sxs-lookup"><span data-stu-id="227fb-117">-Force</span></span>
<span data-ttu-id="227fb-118">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="227fb-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="227fb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="227fb-119">-ResourceGroupName</span></span>
<span data-ttu-id="227fb-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="227fb-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="227fb-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="227fb-121">-Confirm</span></span>
<span data-ttu-id="227fb-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="227fb-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="227fb-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="227fb-123">-WhatIf</span></span>
<span data-ttu-id="227fb-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="227fb-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="227fb-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="227fb-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="227fb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="227fb-126">CommonParameters</span></span>
<span data-ttu-id="227fb-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="227fb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="227fb-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="227fb-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="227fb-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="227fb-129">INPUTS</span></span>

### <span data-ttu-id="227fb-130">System. String</span><span class="sxs-lookup"><span data-stu-id="227fb-130">System.String</span></span>

## <span data-ttu-id="227fb-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="227fb-131">OUTPUTS</span></span>

### <span data-ttu-id="227fb-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="227fb-132">System.Object</span></span>

## <span data-ttu-id="227fb-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="227fb-133">NOTES</span></span>

## <span data-ttu-id="227fb-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="227fb-134">RELATED LINKS</span></span>

