---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 6AB6C366-4925-4370-A33E-EDAF4BE1E230
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/remove-azurermmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Remove-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Remove-AzureRmMediaService.md
ms.openlocfilehash: 373647cfc06c36a510a8208424d00087f00e693e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557307"
---
# <span data-ttu-id="4dd38-101">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="4dd38-101">Remove-AzureRmMediaService</span></span>

## <span data-ttu-id="4dd38-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4dd38-102">SYNOPSIS</span></span>
<span data-ttu-id="4dd38-103">Удаление службы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="4dd38-103">Removes a media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4dd38-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4dd38-104">SYNTAX</span></span>

```
Remove-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4dd38-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4dd38-105">DESCRIPTION</span></span>
<span data-ttu-id="4dd38-106">Командлет **Remove-AzureRmMediaService** Удаляет службу мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="4dd38-106">The **Remove-AzureRmMediaService** cmdlet removes a media service.</span></span>

## <span data-ttu-id="4dd38-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4dd38-107">EXAMPLES</span></span>

### <span data-ttu-id="4dd38-108">Пример 1: Удаление службы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="4dd38-108">Example 1: Remove a media service</span></span>
```
PS C:\>Remove-AzureRmMediaService -ResourceGroupName "ResourceGroup001" -AccountName "MediaService0011"
```

<span data-ttu-id="4dd38-109">Эта команда удаляет службу мультимедиа с именем MediaService0011 в группе ресурсов с именем ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="4dd38-109">This command removes the media service named MediaService0011 in the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="4dd38-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4dd38-110">PARAMETERS</span></span>

### <span data-ttu-id="4dd38-111">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="4dd38-111">-AccountName</span></span>
<span data-ttu-id="4dd38-112">Указывает имя службы мультимедиа, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="4dd38-112">Specifies the name of the media service that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dd38-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dd38-113">-DefaultProfile</span></span>
<span data-ttu-id="4dd38-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4dd38-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4dd38-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4dd38-115">-Force</span></span>
<span data-ttu-id="4dd38-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="4dd38-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4dd38-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dd38-117">-ResourceGroupName</span></span>
<span data-ttu-id="4dd38-118">Указывает имя группы ресурсов, в которой находится служба мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="4dd38-118">Specifies the name of the resource group that contains the media service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dd38-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4dd38-119">-Confirm</span></span>
<span data-ttu-id="4dd38-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4dd38-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dd38-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dd38-121">-WhatIf</span></span>
<span data-ttu-id="4dd38-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4dd38-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dd38-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4dd38-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dd38-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dd38-124">CommonParameters</span></span>
<span data-ttu-id="4dd38-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4dd38-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dd38-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4dd38-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dd38-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4dd38-127">INPUTS</span></span>

### <span data-ttu-id="4dd38-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="4dd38-128">None</span></span>
<span data-ttu-id="4dd38-129">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="4dd38-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4dd38-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4dd38-130">OUTPUTS</span></span>

### <span data-ttu-id="4dd38-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4dd38-131">System.Boolean</span></span>

## <span data-ttu-id="4dd38-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="4dd38-132">NOTES</span></span>

## <span data-ttu-id="4dd38-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4dd38-133">RELATED LINKS</span></span>

[<span data-ttu-id="4dd38-134">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="4dd38-134">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="4dd38-135">New-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="4dd38-135">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="4dd38-136">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="4dd38-136">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


