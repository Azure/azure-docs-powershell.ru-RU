---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmSnapshot.md
ms.openlocfilehash: edd2d89cfe0488021ef62780ade80cb2b98437c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558484"
---
# <span data-ttu-id="f4f2a-101">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="f4f2a-101">Remove-AzureRmSnapshot</span></span>

## <span data-ttu-id="f4f2a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f4f2a-102">SYNOPSIS</span></span>
<span data-ttu-id="f4f2a-103">Удаляет снимок.</span><span class="sxs-lookup"><span data-stu-id="f4f2a-103">Removes a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4f2a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f4f2a-104">SYNTAX</span></span>

```
Remove-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4f2a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4f2a-105">DESCRIPTION</span></span>
<span data-ttu-id="f4f2a-106">Командлет **Remove-AzureRmSnapshot** удаляет моментальный снимок.</span><span class="sxs-lookup"><span data-stu-id="f4f2a-106">The **Remove-AzureRmSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="f4f2a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f4f2a-107">EXAMPLES</span></span>

### <span data-ttu-id="f4f2a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f4f2a-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="f4f2a-109">Эта команда удаляет моментальный снимок с именем "Snapshot01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="f4f2a-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="f4f2a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f4f2a-110">PARAMETERS</span></span>

### <span data-ttu-id="f4f2a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4f2a-111">-AsJob</span></span>
<span data-ttu-id="f4f2a-112">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="f4f2a-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="f4f2a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4f2a-113">-DefaultProfile</span></span>
<span data-ttu-id="f4f2a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f4f2a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4f2a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f4f2a-115">-Force</span></span>
<span data-ttu-id="f4f2a-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="f4f2a-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f4f2a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4f2a-117">-ResourceGroupName</span></span>
<span data-ttu-id="f4f2a-118">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f4f2a-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f4f2a-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="f4f2a-119">-SnapshotName</span></span>
<span data-ttu-id="f4f2a-120">Указывает имя снимка.</span><span class="sxs-lookup"><span data-stu-id="f4f2a-120">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4f2a-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4f2a-121">-Confirm</span></span>
<span data-ttu-id="f4f2a-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f4f2a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4f2a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4f2a-123">-WhatIf</span></span>
<span data-ttu-id="f4f2a-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f4f2a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4f2a-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f4f2a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4f2a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4f2a-126">CommonParameters</span></span>
<span data-ttu-id="f4f2a-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f4f2a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4f2a-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4f2a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4f2a-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f4f2a-129">INPUTS</span></span>

### <span data-ttu-id="f4f2a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f4f2a-130">System.String</span></span>

## <span data-ttu-id="f4f2a-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4f2a-131">OUTPUTS</span></span>

### <span data-ttu-id="f4f2a-132">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="f4f2a-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="f4f2a-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="f4f2a-133">NOTES</span></span>

## <span data-ttu-id="f4f2a-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f4f2a-134">RELATED LINKS</span></span>
