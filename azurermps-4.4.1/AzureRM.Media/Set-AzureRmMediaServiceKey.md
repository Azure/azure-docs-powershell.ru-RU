---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: D28EB28D-DBC6-48D5-AB0A-C56F56CD0104
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaServiceKey.md
ms.openlocfilehash: 7b8c1b154a631a911100f4b2b8581ca552e4b565
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568049"
---
# <span data-ttu-id="d07db-101">Set-AzureRmMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="d07db-101">Set-AzureRmMediaServiceKey</span></span>

## <span data-ttu-id="d07db-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d07db-102">SYNOPSIS</span></span>
<span data-ttu-id="d07db-103">Повторное создание ключа, используемого для доступа к конечной точке RESTFUL, связанной с службой мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="d07db-103">Regenerates a key used for accessing the REST endpoint associated with the media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d07db-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d07db-104">SYNTAX</span></span>

```
Set-AzureRmMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String> [-KeyType] <KeyType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d07db-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d07db-105">DESCRIPTION</span></span>
<span data-ttu-id="d07db-106">Командлет **Set-AzureRmMediaServiceKey** заново создает ключ, который используется для доступа к конечной точке пересылки состояния (RESTful), связанной с службой мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="d07db-106">The **Set-AzureRmMediaServiceKey** cmdlet regenerates a key used for accessing the Representational State Transfer (REST) endpoint associated with the media service.</span></span>

## <span data-ttu-id="d07db-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d07db-107">EXAMPLES</span></span>

### <span data-ttu-id="d07db-108">Пример 1: повторное создание первичного ключа, используемого для доступа к службе мультимедиа</span><span class="sxs-lookup"><span data-stu-id="d07db-108">Example 1: Regenerate the primary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzureRmMediaServiceKey -ResourceGroupName "ResourceGroup004" -AccountName "MediaService001" -KeyType Primary
```

<span data-ttu-id="d07db-109">Эта команда повторно создает первичный ключ для службы мультимедиа с именем MediaService001, который принадлежит группе ресурсов с именем ResourceGroup004.</span><span class="sxs-lookup"><span data-stu-id="d07db-109">This command regenerates the primary key for the media service named MediaService001 that belongs to the resource group named ResourceGroup004.</span></span>

### <span data-ttu-id="d07db-110">Пример 2: повторное создание вторичного ключа, используемого для доступа к службе мультимедиа</span><span class="sxs-lookup"><span data-stu-id="d07db-110">Example 2: Regenerates the secondary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzureRmMediaServiceKey -ResourceGroupName "Resourcegroup123" -AccountName "MediaService002" -KeyType Secondary
```

<span data-ttu-id="d07db-111">Эта команда повторно создает вторичный ключ для службы мультимедиа с именем MediaService002, который принадлежит группе ресурсов с именем Resourcegroup123.</span><span class="sxs-lookup"><span data-stu-id="d07db-111">This command regenerates the secondary key for the media service named MediaService002 that belongs to the resource group named Resourcegroup123.</span></span>

## <span data-ttu-id="d07db-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d07db-112">PARAMETERS</span></span>

### <span data-ttu-id="d07db-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="d07db-113">-AccountName</span></span>
<span data-ttu-id="d07db-114">Указывает имя службы мультимедиа, создаваемой этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="d07db-114">Specifies the name of the media service that this cmdlet regenerates.</span></span>

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

### <span data-ttu-id="d07db-115">-KeyType</span><span class="sxs-lookup"><span data-stu-id="d07db-115">-KeyType</span></span>
<span data-ttu-id="d07db-116">Указывает тип ключа службы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="d07db-116">Specifies the key type of the media service.</span></span>
<span data-ttu-id="d07db-117">Допустимые значения этого параметра: Primary или Secondary.</span><span class="sxs-lookup"><span data-stu-id="d07db-117">The acceptable values for this parameter are: Primary or Secondary.</span></span>

```yaml
Type: Microsoft.Azure.Management.Media.Models.KeyType
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d07db-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d07db-118">-ResourceGroupName</span></span>
<span data-ttu-id="d07db-119">Указывает имя группы ресурсов, в которой находится служба мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="d07db-119">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="d07db-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d07db-120">-Confirm</span></span>
<span data-ttu-id="d07db-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d07db-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d07db-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d07db-122">-WhatIf</span></span>
<span data-ttu-id="d07db-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d07db-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d07db-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d07db-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d07db-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d07db-125">-DefaultProfile</span></span>
<span data-ttu-id="d07db-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d07db-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d07db-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d07db-127">CommonParameters</span></span>
<span data-ttu-id="d07db-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d07db-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d07db-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d07db-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d07db-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d07db-130">INPUTS</span></span>

## <span data-ttu-id="d07db-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d07db-131">OUTPUTS</span></span>

### <span data-ttu-id="d07db-132">Microsoft. Azure. Commands. Media. Models. PSServiceKey</span><span class="sxs-lookup"><span data-stu-id="d07db-132">Microsoft.Azure.Commands.Media.Models.PSServiceKey</span></span>

## <span data-ttu-id="d07db-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="d07db-133">NOTES</span></span>

## <span data-ttu-id="d07db-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d07db-134">RELATED LINKS</span></span>

[<span data-ttu-id="d07db-135">Get-AzureRmMediaServiceKeys</span><span class="sxs-lookup"><span data-stu-id="d07db-135">Get-AzureRmMediaServiceKeys</span></span>](./Get-AzureRmMediaServiceKeys.md)


