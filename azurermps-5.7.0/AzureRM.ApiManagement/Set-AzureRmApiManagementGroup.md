---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
ms.openlocfilehash: 20f2f79c154cd16dcf09501bdbefb488fdeb61eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565031"
---
# <span data-ttu-id="6c511-101">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="6c511-101">Set-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="6c511-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6c511-102">SYNOPSIS</span></span>
<span data-ttu-id="6c511-103">Настраивает группу управления API.</span><span class="sxs-lookup"><span data-stu-id="6c511-103">Configures an API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c511-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6c511-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c511-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6c511-105">DESCRIPTION</span></span>
<span data-ttu-id="6c511-106">Командлет **Set-AzureRmApiManagementGroup** настраивает группу управления API.</span><span class="sxs-lookup"><span data-stu-id="6c511-106">The **Set-AzureRmApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="6c511-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6c511-107">EXAMPLES</span></span>

### <span data-ttu-id="6c511-108">Пример 1: Настройка группы управления</span><span class="sxs-lookup"><span data-stu-id="6c511-108">Example 1: Configure a management group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementGroup -Context $apimContext -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="6c511-109">Эта команда настраивает группу управления с именем Group0001.</span><span class="sxs-lookup"><span data-stu-id="6c511-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="6c511-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6c511-110">PARAMETERS</span></span>

### <span data-ttu-id="6c511-111">-Context</span><span class="sxs-lookup"><span data-stu-id="6c511-111">-Context</span></span>
<span data-ttu-id="6c511-112">Указывает экземпляр объекта **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="6c511-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c511-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c511-113">-DefaultProfile</span></span>
<span data-ttu-id="6c511-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6c511-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="6c511-115">-Описание</span><span class="sxs-lookup"><span data-stu-id="6c511-115">-Description</span></span>
<span data-ttu-id="6c511-116">Задает описание группы управления.</span><span class="sxs-lookup"><span data-stu-id="6c511-116">Specifies the description of the management group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c511-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="6c511-117">-GroupId</span></span>
<span data-ttu-id="6c511-118">Указывает идентификатор группы управления.</span><span class="sxs-lookup"><span data-stu-id="6c511-118">Specifies the identifier of the management group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c511-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6c511-119">-Name</span></span>
<span data-ttu-id="6c511-120">Указывает имя группы управления.</span><span class="sxs-lookup"><span data-stu-id="6c511-120">Specifies the name of the management group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c511-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6c511-121">-PassThru</span></span>
<span data-ttu-id="6c511-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="6c511-122">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c511-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c511-123">CommonParameters</span></span>
<span data-ttu-id="6c511-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6c511-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c511-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c511-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c511-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6c511-126">INPUTS</span></span>

### <span data-ttu-id="6c511-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="6c511-127">None</span></span>
<span data-ttu-id="6c511-128">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="6c511-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6c511-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6c511-129">OUTPUTS</span></span>

### <span data-ttu-id="6c511-130">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="6c511-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="6c511-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="6c511-131">NOTES</span></span>

## <span data-ttu-id="6c511-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6c511-132">RELATED LINKS</span></span>

[<span data-ttu-id="6c511-133">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="6c511-133">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="6c511-134">New-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="6c511-134">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="6c511-135">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="6c511-135">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)


