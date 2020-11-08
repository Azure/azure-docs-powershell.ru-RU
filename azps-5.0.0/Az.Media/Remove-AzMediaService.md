---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 6AB6C366-4925-4370-A33E-EDAF4BE1E230
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/remove-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
ms.openlocfilehash: 525c5e2bfd15811e861945a6404e0b88274e2563
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248883"
---
# <span data-ttu-id="816d8-101">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="816d8-101">Remove-AzMediaService</span></span>

## <span data-ttu-id="816d8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="816d8-102">SYNOPSIS</span></span>
<span data-ttu-id="816d8-103">Удаление службы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="816d8-103">Removes a media service.</span></span>

## <span data-ttu-id="816d8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="816d8-104">SYNTAX</span></span>

```
Remove-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="816d8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="816d8-105">DESCRIPTION</span></span>
<span data-ttu-id="816d8-106">Командлет **Remove-AzMediaService** Удаляет службу мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="816d8-106">The **Remove-AzMediaService** cmdlet removes a media service.</span></span>

## <span data-ttu-id="816d8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="816d8-107">EXAMPLES</span></span>

### <span data-ttu-id="816d8-108">Пример 1: Удаление службы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="816d8-108">Example 1: Remove a media service</span></span>
```
PS C:\>Remove-AzMediaService -ResourceGroupName "ResourceGroup001" -AccountName "MediaService0011"
```

<span data-ttu-id="816d8-109">Эта команда удаляет службу мультимедиа с именем MediaService0011 в группе ресурсов с именем ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="816d8-109">This command removes the media service named MediaService0011 in the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="816d8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="816d8-110">PARAMETERS</span></span>

### <span data-ttu-id="816d8-111">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="816d8-111">-AccountName</span></span>
<span data-ttu-id="816d8-112">Указывает имя службы мультимедиа, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="816d8-112">Specifies the name of the media service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="816d8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="816d8-113">-DefaultProfile</span></span>
<span data-ttu-id="816d8-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="816d8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="816d8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="816d8-115">-Force</span></span>
<span data-ttu-id="816d8-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="816d8-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="816d8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="816d8-117">-ResourceGroupName</span></span>
<span data-ttu-id="816d8-118">Указывает имя группы ресурсов, в которой находится служба мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="816d8-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="816d8-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="816d8-119">-Confirm</span></span>
<span data-ttu-id="816d8-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="816d8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="816d8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="816d8-121">-WhatIf</span></span>
<span data-ttu-id="816d8-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="816d8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="816d8-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="816d8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="816d8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="816d8-124">CommonParameters</span></span>
<span data-ttu-id="816d8-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="816d8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="816d8-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="816d8-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="816d8-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="816d8-127">INPUTS</span></span>

### <span data-ttu-id="816d8-128">System. String</span><span class="sxs-lookup"><span data-stu-id="816d8-128">System.String</span></span>

## <span data-ttu-id="816d8-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="816d8-129">OUTPUTS</span></span>

### <span data-ttu-id="816d8-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="816d8-130">System.Boolean</span></span>

## <span data-ttu-id="816d8-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="816d8-131">NOTES</span></span>

## <span data-ttu-id="816d8-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="816d8-132">RELATED LINKS</span></span>

[<span data-ttu-id="816d8-133">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="816d8-133">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="816d8-134">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="816d8-134">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="816d8-135">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="816d8-135">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


