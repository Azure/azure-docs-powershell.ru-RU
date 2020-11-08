---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 6AB6C366-4925-4370-A33E-EDAF4BE1E230
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/remove-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
ms.openlocfilehash: 525c5e2bfd15811e861945a6404e0b88274e2563
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074531"
---
# <span data-ttu-id="788e3-101">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="788e3-101">Remove-AzMediaService</span></span>

## <span data-ttu-id="788e3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="788e3-102">SYNOPSIS</span></span>
<span data-ttu-id="788e3-103">Удаление службы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="788e3-103">Removes a media service.</span></span>

## <span data-ttu-id="788e3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="788e3-104">SYNTAX</span></span>

```
Remove-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="788e3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="788e3-105">DESCRIPTION</span></span>
<span data-ttu-id="788e3-106">Командлет **Remove-AzMediaService** Удаляет службу мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="788e3-106">The **Remove-AzMediaService** cmdlet removes a media service.</span></span>

## <span data-ttu-id="788e3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="788e3-107">EXAMPLES</span></span>

### <span data-ttu-id="788e3-108">Пример 1: Удаление службы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="788e3-108">Example 1: Remove a media service</span></span>
```
PS C:\>Remove-AzMediaService -ResourceGroupName "ResourceGroup001" -AccountName "MediaService0011"
```

<span data-ttu-id="788e3-109">Эта команда удаляет службу мультимедиа с именем MediaService0011 в группе ресурсов с именем ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="788e3-109">This command removes the media service named MediaService0011 in the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="788e3-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="788e3-110">PARAMETERS</span></span>

### <span data-ttu-id="788e3-111">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="788e3-111">-AccountName</span></span>
<span data-ttu-id="788e3-112">Указывает имя службы мультимедиа, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="788e3-112">Specifies the name of the media service that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="788e3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="788e3-113">-DefaultProfile</span></span>
<span data-ttu-id="788e3-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="788e3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="788e3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="788e3-115">-Force</span></span>
<span data-ttu-id="788e3-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="788e3-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="788e3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="788e3-117">-ResourceGroupName</span></span>
<span data-ttu-id="788e3-118">Указывает имя группы ресурсов, в которой находится служба мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="788e3-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="788e3-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="788e3-119">-Confirm</span></span>
<span data-ttu-id="788e3-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="788e3-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="788e3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="788e3-121">-WhatIf</span></span>
<span data-ttu-id="788e3-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="788e3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="788e3-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="788e3-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="788e3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="788e3-124">CommonParameters</span></span>
<span data-ttu-id="788e3-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="788e3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="788e3-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="788e3-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="788e3-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="788e3-127">INPUTS</span></span>

### <span data-ttu-id="788e3-128">System. String</span><span class="sxs-lookup"><span data-stu-id="788e3-128">System.String</span></span>

## <span data-ttu-id="788e3-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="788e3-129">OUTPUTS</span></span>

### <span data-ttu-id="788e3-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="788e3-130">System.Boolean</span></span>

## <span data-ttu-id="788e3-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="788e3-131">NOTES</span></span>

## <span data-ttu-id="788e3-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="788e3-132">RELATED LINKS</span></span>

[<span data-ttu-id="788e3-133">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="788e3-133">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="788e3-134">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="788e3-134">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="788e3-135">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="788e3-135">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


