---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 6AB6C366-4925-4370-A33E-EDAF4BE1E230
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/remove-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
ms.openlocfilehash: f9d0ee722f828aba251c9776c231338b54c0580c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93899641"
---
# <span data-ttu-id="16dba-101">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="16dba-101">Remove-AzMediaService</span></span>

## <span data-ttu-id="16dba-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="16dba-102">SYNOPSIS</span></span>
<span data-ttu-id="16dba-103">Удаление службы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="16dba-103">Removes a media service.</span></span>

## <span data-ttu-id="16dba-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="16dba-104">SYNTAX</span></span>

```
Remove-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16dba-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="16dba-105">DESCRIPTION</span></span>
<span data-ttu-id="16dba-106">Командлет **Remove-AzMediaService** Удаляет службу мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="16dba-106">The **Remove-AzMediaService** cmdlet removes a media service.</span></span>

## <span data-ttu-id="16dba-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="16dba-107">EXAMPLES</span></span>

### <span data-ttu-id="16dba-108">Пример 1: Удаление службы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="16dba-108">Example 1: Remove a media service</span></span>
```
PS C:\>Remove-AzMediaService -ResourceGroupName "ResourceGroup001" -AccountName "MediaService0011"
```

<span data-ttu-id="16dba-109">Эта команда удаляет службу мультимедиа с именем MediaService0011 в группе ресурсов с именем ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="16dba-109">This command removes the media service named MediaService0011 in the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="16dba-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="16dba-110">PARAMETERS</span></span>

### <span data-ttu-id="16dba-111">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="16dba-111">-AccountName</span></span>
<span data-ttu-id="16dba-112">Указывает имя службы мультимедиа, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="16dba-112">Specifies the name of the media service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="16dba-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16dba-113">-DefaultProfile</span></span>
<span data-ttu-id="16dba-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="16dba-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16dba-115">-Force</span><span class="sxs-lookup"><span data-stu-id="16dba-115">-Force</span></span>
<span data-ttu-id="16dba-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="16dba-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="16dba-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16dba-117">-ResourceGroupName</span></span>
<span data-ttu-id="16dba-118">Указывает имя группы ресурсов, в которой находится служба мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="16dba-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="16dba-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="16dba-119">-Confirm</span></span>
<span data-ttu-id="16dba-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="16dba-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16dba-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16dba-121">-WhatIf</span></span>
<span data-ttu-id="16dba-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="16dba-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16dba-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="16dba-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16dba-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16dba-124">CommonParameters</span></span>
<span data-ttu-id="16dba-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="16dba-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16dba-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16dba-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16dba-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="16dba-127">INPUTS</span></span>

### <span data-ttu-id="16dba-128">System. String</span><span class="sxs-lookup"><span data-stu-id="16dba-128">System.String</span></span>

## <span data-ttu-id="16dba-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="16dba-129">OUTPUTS</span></span>

### <span data-ttu-id="16dba-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="16dba-130">System.Boolean</span></span>

## <span data-ttu-id="16dba-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="16dba-131">NOTES</span></span>

## <span data-ttu-id="16dba-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="16dba-132">RELATED LINKS</span></span>

[<span data-ttu-id="16dba-133">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="16dba-133">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="16dba-134">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="16dba-134">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="16dba-135">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="16dba-135">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


