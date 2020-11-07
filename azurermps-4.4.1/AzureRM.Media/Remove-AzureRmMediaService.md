---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 6AB6C366-4925-4370-A33E-EDAF4BE1E230
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Remove-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Remove-AzureRmMediaService.md
ms.openlocfilehash: 9507cc178613a80ff0d49ed62e7e43698f5f1d7c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733699"
---
# <span data-ttu-id="837d8-101">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="837d8-101">Remove-AzureRmMediaService</span></span>

## <span data-ttu-id="837d8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="837d8-102">SYNOPSIS</span></span>
<span data-ttu-id="837d8-103">Удаление службы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="837d8-103">Removes a media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="837d8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="837d8-104">SYNTAX</span></span>

```
Remove-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="837d8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="837d8-105">DESCRIPTION</span></span>
<span data-ttu-id="837d8-106">Командлет **Remove-AzureRmMediaService** Удаляет службу мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="837d8-106">The **Remove-AzureRmMediaService** cmdlet removes a media service.</span></span>

## <span data-ttu-id="837d8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="837d8-107">EXAMPLES</span></span>

### <span data-ttu-id="837d8-108">Пример 1: Удаление службы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="837d8-108">Example 1: Remove a media service</span></span>
```
PS C:\>Remove-AzureRmMediaService -ResourceGroupName "ResourceGroup001" -AccountName "MediaService0011"
```

<span data-ttu-id="837d8-109">Эта команда удаляет службу мультимедиа с именем MediaService0011 в группе ресурсов с именем ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="837d8-109">This command removes the media service named MediaService0011 in the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="837d8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="837d8-110">PARAMETERS</span></span>

### <span data-ttu-id="837d8-111">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="837d8-111">-AccountName</span></span>
<span data-ttu-id="837d8-112">Указывает имя службы мультимедиа, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="837d8-112">Specifies the name of the media service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="837d8-113">-Force</span><span class="sxs-lookup"><span data-stu-id="837d8-113">-Force</span></span>
<span data-ttu-id="837d8-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="837d8-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="837d8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="837d8-115">-ResourceGroupName</span></span>
<span data-ttu-id="837d8-116">Указывает имя группы ресурсов, в которой находится служба мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="837d8-116">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="837d8-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="837d8-117">-Confirm</span></span>
<span data-ttu-id="837d8-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="837d8-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="837d8-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="837d8-119">-WhatIf</span></span>
<span data-ttu-id="837d8-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="837d8-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="837d8-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="837d8-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="837d8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="837d8-122">-DefaultProfile</span></span>
<span data-ttu-id="837d8-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="837d8-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="837d8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="837d8-124">CommonParameters</span></span>
<span data-ttu-id="837d8-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="837d8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="837d8-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="837d8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="837d8-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="837d8-127">INPUTS</span></span>

## <span data-ttu-id="837d8-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="837d8-128">OUTPUTS</span></span>

### <span data-ttu-id="837d8-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="837d8-129">System.Boolean</span></span>

## <span data-ttu-id="837d8-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="837d8-130">NOTES</span></span>

## <span data-ttu-id="837d8-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="837d8-131">RELATED LINKS</span></span>

[<span data-ttu-id="837d8-132">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="837d8-132">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="837d8-133">New-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="837d8-133">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="837d8-134">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="837d8-134">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


