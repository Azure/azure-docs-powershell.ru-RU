---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmSnapshot.md
ms.openlocfilehash: 4c7260d3c1131ab573bf933f4b83022cef20819d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569612"
---
# <span data-ttu-id="75bd1-101">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="75bd1-101">Remove-AzureRmSnapshot</span></span>

## <span data-ttu-id="75bd1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="75bd1-102">SYNOPSIS</span></span>
<span data-ttu-id="75bd1-103">Удаляет снимок.</span><span class="sxs-lookup"><span data-stu-id="75bd1-103">Removes a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75bd1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="75bd1-104">SYNTAX</span></span>

```
Remove-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75bd1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="75bd1-105">DESCRIPTION</span></span>
<span data-ttu-id="75bd1-106">Командлет **Remove-AzureRmSnapshot** удаляет моментальный снимок.</span><span class="sxs-lookup"><span data-stu-id="75bd1-106">The **Remove-AzureRmSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="75bd1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="75bd1-107">EXAMPLES</span></span>

### <span data-ttu-id="75bd1-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="75bd1-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="75bd1-109">Эта команда удаляет моментальный снимок с именем "Snapshot01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="75bd1-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="75bd1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="75bd1-110">PARAMETERS</span></span>

### <span data-ttu-id="75bd1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75bd1-111">-DefaultProfile</span></span>
<span data-ttu-id="75bd1-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="75bd1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75bd1-113">-Force</span><span class="sxs-lookup"><span data-stu-id="75bd1-113">-Force</span></span>
<span data-ttu-id="75bd1-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="75bd1-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="75bd1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75bd1-115">-ResourceGroupName</span></span>
<span data-ttu-id="75bd1-116">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="75bd1-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="75bd1-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="75bd1-117">-SnapshotName</span></span>
<span data-ttu-id="75bd1-118">Указывает имя снимка.</span><span class="sxs-lookup"><span data-stu-id="75bd1-118">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="75bd1-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75bd1-119">-Confirm</span></span>
<span data-ttu-id="75bd1-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="75bd1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75bd1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75bd1-121">-WhatIf</span></span>
<span data-ttu-id="75bd1-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="75bd1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75bd1-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="75bd1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75bd1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75bd1-124">CommonParameters</span></span>
<span data-ttu-id="75bd1-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="75bd1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75bd1-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75bd1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75bd1-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="75bd1-127">INPUTS</span></span>

### <span data-ttu-id="75bd1-128">System. String</span><span class="sxs-lookup"><span data-stu-id="75bd1-128">System.String</span></span>

## <span data-ttu-id="75bd1-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="75bd1-129">OUTPUTS</span></span>

### <span data-ttu-id="75bd1-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="75bd1-130">System.Object</span></span>

## <span data-ttu-id="75bd1-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="75bd1-131">NOTES</span></span>

## <span data-ttu-id="75bd1-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="75bd1-132">RELATED LINKS</span></span>

