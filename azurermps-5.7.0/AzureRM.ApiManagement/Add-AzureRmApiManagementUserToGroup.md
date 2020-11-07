---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementusertogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
ms.openlocfilehash: 300c99926ae7f58a6bf53ba49f3b5b86f243e150
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733594"
---
# <span data-ttu-id="5e8cb-101">Add-AzureRmApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="5e8cb-101">Add-AzureRmApiManagementUserToGroup</span></span>

## <span data-ttu-id="5e8cb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5e8cb-102">SYNOPSIS</span></span>
<span data-ttu-id="5e8cb-103">Добавляет пользователя в группу.</span><span class="sxs-lookup"><span data-stu-id="5e8cb-103">Adds a user to a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e8cb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5e8cb-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e8cb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e8cb-105">DESCRIPTION</span></span>
<span data-ttu-id="5e8cb-106">Командлет **Add-AzureRmApiManagementUserToGroup** добавляет пользователя в группу.</span><span class="sxs-lookup"><span data-stu-id="5e8cb-106">The **Add-AzureRmApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="5e8cb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5e8cb-107">EXAMPLES</span></span>

### <span data-ttu-id="5e8cb-108">Пример 1: Добавление пользователя в группу</span><span class="sxs-lookup"><span data-stu-id="5e8cb-108">Example 1: Add a user to a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzureRmApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="5e8cb-109">Эта команда добавляет существующего пользователя в существующую группу.</span><span class="sxs-lookup"><span data-stu-id="5e8cb-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="5e8cb-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5e8cb-110">PARAMETERS</span></span>

### <span data-ttu-id="5e8cb-111">-Context</span><span class="sxs-lookup"><span data-stu-id="5e8cb-111">-Context</span></span>
<span data-ttu-id="5e8cb-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="5e8cb-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="5e8cb-113">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="5e8cb-113">This parameter is required.</span></span>

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

### <span data-ttu-id="5e8cb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e8cb-114">-DefaultProfile</span></span>
<span data-ttu-id="5e8cb-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5e8cb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="5e8cb-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="5e8cb-116">-GroupId</span></span>
<span data-ttu-id="5e8cb-117">Указывает код группы.</span><span class="sxs-lookup"><span data-stu-id="5e8cb-117">Specifies the group ID.</span></span>
<span data-ttu-id="5e8cb-118">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="5e8cb-118">This parameter is required.</span></span>

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

### <span data-ttu-id="5e8cb-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e8cb-119">-PassThru</span></span>
<span data-ttu-id="5e8cb-120">PassThru</span><span class="sxs-lookup"><span data-stu-id="5e8cb-120">passthru</span></span>

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

### <span data-ttu-id="5e8cb-121">-UserId</span><span class="sxs-lookup"><span data-stu-id="5e8cb-121">-UserId</span></span>
<span data-ttu-id="5e8cb-122">Указывает идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="5e8cb-122">Specifies the user ID.</span></span>
<span data-ttu-id="5e8cb-123">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="5e8cb-123">This parameter is required.</span></span>

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

### <span data-ttu-id="5e8cb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e8cb-124">CommonParameters</span></span>
<span data-ttu-id="5e8cb-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5e8cb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e8cb-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e8cb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e8cb-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5e8cb-127">INPUTS</span></span>

### <span data-ttu-id="5e8cb-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="5e8cb-128">None</span></span>
<span data-ttu-id="5e8cb-129">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="5e8cb-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5e8cb-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e8cb-130">OUTPUTS</span></span>

### <span data-ttu-id="5e8cb-131">Значением</span><span class="sxs-lookup"><span data-stu-id="5e8cb-131">Boolean</span></span>

## <span data-ttu-id="5e8cb-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="5e8cb-132">NOTES</span></span>

## <span data-ttu-id="5e8cb-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5e8cb-133">RELATED LINKS</span></span>

[<span data-ttu-id="5e8cb-134">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="5e8cb-134">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="5e8cb-135">Remove-AzureRmApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="5e8cb-135">Remove-AzureRmApiManagementUserFromGroup</span></span>](./Remove-AzureRmApiManagementUserFromGroup.md)


