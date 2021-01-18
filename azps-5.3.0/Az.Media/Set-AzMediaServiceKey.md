---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: D28EB28D-DBC6-48D5-AB0A-C56F56CD0104
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/set-azmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaServiceKey.md
ms.openlocfilehash: 44c1ff2fe283e3cd804d20a8df21023b3c222150
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98520020"
---
# <span data-ttu-id="ac329-101">Set-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="ac329-101">Set-AzMediaServiceKey</span></span>

## <span data-ttu-id="ac329-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac329-102">SYNOPSIS</span></span>
<span data-ttu-id="ac329-103">Повторно сгенерирует ключ, используемый для доступа к конечной точке REST, связанной со службой мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ac329-103">Regenerates a key used for accessing the REST endpoint associated with the media service.</span></span>

## <span data-ttu-id="ac329-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ac329-104">SYNTAX</span></span>

```
Set-AzMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String> [-KeyType] <KeyType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac329-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac329-105">DESCRIPTION</span></span>
<span data-ttu-id="ac329-106">С **помощью cmdlet Set-AzMediaServiceKey** можно сгенерировать ключ, используемый для доступа к конечной точке REST, связанной со службой мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ac329-106">The **Set-AzMediaServiceKey** cmdlet regenerates a key used for accessing the Representational State Transfer (REST) endpoint associated with the media service.</span></span>

## <span data-ttu-id="ac329-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ac329-107">EXAMPLES</span></span>

### <span data-ttu-id="ac329-108">Пример 1. Повторное сгенерировать первичный ключ, используемый для доступа к службе мультимедиа</span><span class="sxs-lookup"><span data-stu-id="ac329-108">Example 1: Regenerate the primary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzMediaServiceKey -ResourceGroupName "ResourceGroup004" -AccountName "MediaService001" -KeyType Primary
```

<span data-ttu-id="ac329-109">Эта команда повторно сгенерирует первичный ключ для службы мультимедиа MediaService001, которая принадлежит к группе ресурсов ResourceGroup004.</span><span class="sxs-lookup"><span data-stu-id="ac329-109">This command regenerates the primary key for the media service named MediaService001 that belongs to the resource group named ResourceGroup004.</span></span>

### <span data-ttu-id="ac329-110">Пример 2. Повторное сгенерирует дополнительный ключ, используемый для доступа к службе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ac329-110">Example 2: Regenerates the secondary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzMediaServiceKey -ResourceGroupName "Resourcegroup123" -AccountName "MediaService002" -KeyType Secondary
```

<span data-ttu-id="ac329-111">Эта команда повторно сгенерирует дополнительный ключ для службы мультимедиа MediaService002, которая принадлежит к группе ресурсов Resourcegroup123.</span><span class="sxs-lookup"><span data-stu-id="ac329-111">This command regenerates the secondary key for the media service named MediaService002 that belongs to the resource group named Resourcegroup123.</span></span>

## <span data-ttu-id="ac329-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac329-112">PARAMETERS</span></span>

### <span data-ttu-id="ac329-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ac329-113">-AccountName</span></span>
<span data-ttu-id="ac329-114">Указывает имя службы мультимедиа, которую сгенерирует этот cmderate.</span><span class="sxs-lookup"><span data-stu-id="ac329-114">Specifies the name of the media service that this cmdlet regenerates.</span></span>

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

### <span data-ttu-id="ac329-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac329-115">-DefaultProfile</span></span>
<span data-ttu-id="ac329-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ac329-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ac329-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="ac329-117">-KeyType</span></span>
<span data-ttu-id="ac329-118">Указывает ключевой тип службы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ac329-118">Specifies the key type of the media service.</span></span>
<span data-ttu-id="ac329-119">Допустимыми значениями для этого параметра являются первичный или дополнительный.</span><span class="sxs-lookup"><span data-stu-id="ac329-119">The acceptable values for this parameter are: Primary or Secondary.</span></span>

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

### <span data-ttu-id="ac329-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac329-120">-ResourceGroupName</span></span>
<span data-ttu-id="ac329-121">Имя группы ресурсов, которая содержит службу мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ac329-121">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="ac329-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac329-122">-Confirm</span></span>
<span data-ttu-id="ac329-123">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac329-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac329-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac329-124">-WhatIf</span></span>
<span data-ttu-id="ac329-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac329-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac329-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ac329-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac329-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac329-127">CommonParameters</span></span>
<span data-ttu-id="ac329-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac329-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac329-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac329-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac329-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ac329-130">INPUTS</span></span>

### <span data-ttu-id="ac329-131">System.String</span><span class="sxs-lookup"><span data-stu-id="ac329-131">System.String</span></span>

## <span data-ttu-id="ac329-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ac329-132">OUTPUTS</span></span>

### <span data-ttu-id="ac329-133">Microsoft.Azure.Commands.Media.Models.PSServiceKey</span><span class="sxs-lookup"><span data-stu-id="ac329-133">Microsoft.Azure.Commands.Media.Models.PSServiceKey</span></span>

## <span data-ttu-id="ac329-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ac329-134">NOTES</span></span>

## <span data-ttu-id="ac329-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ac329-135">RELATED LINKS</span></span>

[<span data-ttu-id="ac329-136">Get-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="ac329-136">Get-AzMediaServiceKey</span></span>](./Get-AzMediaServiceKey.md)


