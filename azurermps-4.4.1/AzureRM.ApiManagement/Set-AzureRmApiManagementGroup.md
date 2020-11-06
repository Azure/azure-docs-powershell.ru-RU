---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
ms.openlocfilehash: 99c5cef4a15619da455b3e7ba1c7891652b991f9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568349"
---
# <span data-ttu-id="c1318-101">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="c1318-101">Set-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="c1318-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c1318-102">SYNOPSIS</span></span>
<span data-ttu-id="c1318-103">Настраивает группу управления API.</span><span class="sxs-lookup"><span data-stu-id="c1318-103">Configures an API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1318-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c1318-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1318-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1318-105">DESCRIPTION</span></span>
<span data-ttu-id="c1318-106">Командлет **Set-AzureRmApiManagementGroup** настраивает группу управления API.</span><span class="sxs-lookup"><span data-stu-id="c1318-106">The **Set-AzureRmApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="c1318-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c1318-107">EXAMPLES</span></span>

### <span data-ttu-id="c1318-108">Пример 1: Настройка группы управления</span><span class="sxs-lookup"><span data-stu-id="c1318-108">Example 1: Configure a management group</span></span>
```
PS C:\>Set-AzureRmApiManagementGroup -Context $APImContext -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="c1318-109">Эта команда настраивает группу управления с именем Group0001.</span><span class="sxs-lookup"><span data-stu-id="c1318-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="c1318-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c1318-110">PARAMETERS</span></span>

### <span data-ttu-id="c1318-111">-Context</span><span class="sxs-lookup"><span data-stu-id="c1318-111">-Context</span></span>
<span data-ttu-id="c1318-112">Указывает экземпляр объекта **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="c1318-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1318-113">-Описание</span><span class="sxs-lookup"><span data-stu-id="c1318-113">-Description</span></span>
<span data-ttu-id="c1318-114">Задает описание группы управления.</span><span class="sxs-lookup"><span data-stu-id="c1318-114">Specifies the description of the management group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1318-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="c1318-115">-GroupId</span></span>
<span data-ttu-id="c1318-116">Указывает идентификатор группы управления.</span><span class="sxs-lookup"><span data-stu-id="c1318-116">Specifies the identifier of the management group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1318-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c1318-117">-Name</span></span>
<span data-ttu-id="c1318-118">Указывает имя группы управления.</span><span class="sxs-lookup"><span data-stu-id="c1318-118">Specifies the name of the management group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1318-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c1318-119">-PassThru</span></span>
<span data-ttu-id="c1318-120">PassThru</span><span class="sxs-lookup"><span data-stu-id="c1318-120">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1318-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1318-121">-DefaultProfile</span></span>
<span data-ttu-id="c1318-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c1318-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1318-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1318-123">CommonParameters</span></span>
<span data-ttu-id="c1318-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c1318-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1318-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1318-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1318-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c1318-126">INPUTS</span></span>

## <span data-ttu-id="c1318-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1318-127">OUTPUTS</span></span>

### <span data-ttu-id="c1318-128">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="c1318-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="c1318-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="c1318-129">NOTES</span></span>

## <span data-ttu-id="c1318-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c1318-130">RELATED LINKS</span></span>

[<span data-ttu-id="c1318-131">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="c1318-131">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="c1318-132">New-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="c1318-132">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="c1318-133">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="c1318-133">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)


