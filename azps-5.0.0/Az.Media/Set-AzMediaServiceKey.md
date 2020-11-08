---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: D28EB28D-DBC6-48D5-AB0A-C56F56CD0104
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/set-azmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaServiceKey.md
ms.openlocfilehash: 44c1ff2fe283e3cd804d20a8df21023b3c222150
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248884"
---
# <span data-ttu-id="f6c6f-101">Set-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="f6c6f-101">Set-AzMediaServiceKey</span></span>

## <span data-ttu-id="f6c6f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f6c6f-102">SYNOPSIS</span></span>
<span data-ttu-id="f6c6f-103">Повторное создание ключа, используемого для доступа к конечной точке RESTFUL, связанной с службой мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f6c6f-103">Regenerates a key used for accessing the REST endpoint associated with the media service.</span></span>

## <span data-ttu-id="f6c6f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f6c6f-104">SYNTAX</span></span>

```
Set-AzMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String> [-KeyType] <KeyType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6c6f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6c6f-105">DESCRIPTION</span></span>
<span data-ttu-id="f6c6f-106">Командлет **Set-AzMediaServiceKey** заново создает ключ, который используется для доступа к конечной точке пересылки состояния (RESTful), связанной с службой мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f6c6f-106">The **Set-AzMediaServiceKey** cmdlet regenerates a key used for accessing the Representational State Transfer (REST) endpoint associated with the media service.</span></span>

## <span data-ttu-id="f6c6f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f6c6f-107">EXAMPLES</span></span>

### <span data-ttu-id="f6c6f-108">Пример 1: повторное создание первичного ключа, используемого для доступа к службе мультимедиа</span><span class="sxs-lookup"><span data-stu-id="f6c6f-108">Example 1: Regenerate the primary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzMediaServiceKey -ResourceGroupName "ResourceGroup004" -AccountName "MediaService001" -KeyType Primary
```

<span data-ttu-id="f6c6f-109">Эта команда повторно создает первичный ключ для службы мультимедиа с именем MediaService001, который принадлежит группе ресурсов с именем ResourceGroup004.</span><span class="sxs-lookup"><span data-stu-id="f6c6f-109">This command regenerates the primary key for the media service named MediaService001 that belongs to the resource group named ResourceGroup004.</span></span>

### <span data-ttu-id="f6c6f-110">Пример 2: повторное создание вторичного ключа, используемого для доступа к службе мультимедиа</span><span class="sxs-lookup"><span data-stu-id="f6c6f-110">Example 2: Regenerates the secondary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzMediaServiceKey -ResourceGroupName "Resourcegroup123" -AccountName "MediaService002" -KeyType Secondary
```

<span data-ttu-id="f6c6f-111">Эта команда повторно создает вторичный ключ для службы мультимедиа с именем MediaService002, который принадлежит группе ресурсов с именем Resourcegroup123.</span><span class="sxs-lookup"><span data-stu-id="f6c6f-111">This command regenerates the secondary key for the media service named MediaService002 that belongs to the resource group named Resourcegroup123.</span></span>

## <span data-ttu-id="f6c6f-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f6c6f-112">PARAMETERS</span></span>

### <span data-ttu-id="f6c6f-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="f6c6f-113">-AccountName</span></span>
<span data-ttu-id="f6c6f-114">Указывает имя службы мультимедиа, создаваемой этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="f6c6f-114">Specifies the name of the media service that this cmdlet regenerates.</span></span>

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

### <span data-ttu-id="f6c6f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6c6f-115">-DefaultProfile</span></span>
<span data-ttu-id="f6c6f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f6c6f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6c6f-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="f6c6f-117">-KeyType</span></span>
<span data-ttu-id="f6c6f-118">Указывает тип ключа службы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f6c6f-118">Specifies the key type of the media service.</span></span>
<span data-ttu-id="f6c6f-119">Допустимые значения этого параметра: Primary или Secondary.</span><span class="sxs-lookup"><span data-stu-id="f6c6f-119">The acceptable values for this parameter are: Primary or Secondary.</span></span>

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

### <span data-ttu-id="f6c6f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6c6f-120">-ResourceGroupName</span></span>
<span data-ttu-id="f6c6f-121">Указывает имя группы ресурсов, в которой находится служба мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f6c6f-121">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="f6c6f-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f6c6f-122">-Confirm</span></span>
<span data-ttu-id="f6c6f-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f6c6f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6c6f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6c6f-124">-WhatIf</span></span>
<span data-ttu-id="f6c6f-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f6c6f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6c6f-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f6c6f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6c6f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6c6f-127">CommonParameters</span></span>
<span data-ttu-id="f6c6f-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f6c6f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6c6f-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6c6f-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6c6f-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f6c6f-130">INPUTS</span></span>

### <span data-ttu-id="f6c6f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="f6c6f-131">System.String</span></span>

## <span data-ttu-id="f6c6f-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6c6f-132">OUTPUTS</span></span>

### <span data-ttu-id="f6c6f-133">Microsoft. Azure. Commands. Media. Models. PSServiceKey</span><span class="sxs-lookup"><span data-stu-id="f6c6f-133">Microsoft.Azure.Commands.Media.Models.PSServiceKey</span></span>

## <span data-ttu-id="f6c6f-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="f6c6f-134">NOTES</span></span>

## <span data-ttu-id="f6c6f-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f6c6f-135">RELATED LINKS</span></span>

[<span data-ttu-id="f6c6f-136">Get-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="f6c6f-136">Get-AzMediaServiceKey</span></span>](./Get-AzMediaServiceKey.md)


