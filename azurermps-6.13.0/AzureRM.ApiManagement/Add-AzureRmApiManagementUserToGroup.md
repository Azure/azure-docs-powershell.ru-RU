---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementusertogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
ms.openlocfilehash: abb86f40c9ac4a2ca04e0f14500df6c39e550dc3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567335"
---
# <span data-ttu-id="b1df2-101">Add-AzureRmApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="b1df2-101">Add-AzureRmApiManagementUserToGroup</span></span>

## <span data-ttu-id="b1df2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b1df2-102">SYNOPSIS</span></span>
<span data-ttu-id="b1df2-103">Добавляет пользователя в группу.</span><span class="sxs-lookup"><span data-stu-id="b1df2-103">Adds a user to a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1df2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b1df2-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1df2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1df2-105">DESCRIPTION</span></span>
<span data-ttu-id="b1df2-106">Командлет **Add-AzureRmApiManagementUserToGroup** добавляет пользователя в группу.</span><span class="sxs-lookup"><span data-stu-id="b1df2-106">The **Add-AzureRmApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="b1df2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b1df2-107">EXAMPLES</span></span>

### <span data-ttu-id="b1df2-108">Пример 1: Добавление пользователя в группу</span><span class="sxs-lookup"><span data-stu-id="b1df2-108">Example 1: Add a user to a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzureRmApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="b1df2-109">Эта команда добавляет существующего пользователя в существующую группу.</span><span class="sxs-lookup"><span data-stu-id="b1df2-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="b1df2-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b1df2-110">PARAMETERS</span></span>

### <span data-ttu-id="b1df2-111">-Context</span><span class="sxs-lookup"><span data-stu-id="b1df2-111">-Context</span></span>
<span data-ttu-id="b1df2-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="b1df2-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="b1df2-113">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="b1df2-113">This parameter is required.</span></span>

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

### <span data-ttu-id="b1df2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1df2-114">-DefaultProfile</span></span>
<span data-ttu-id="b1df2-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b1df2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1df2-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="b1df2-116">-GroupId</span></span>
<span data-ttu-id="b1df2-117">Указывает код группы.</span><span class="sxs-lookup"><span data-stu-id="b1df2-117">Specifies the group ID.</span></span>
<span data-ttu-id="b1df2-118">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="b1df2-118">This parameter is required.</span></span>

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

### <span data-ttu-id="b1df2-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b1df2-119">-PassThru</span></span>
<span data-ttu-id="b1df2-120">PassThru</span><span class="sxs-lookup"><span data-stu-id="b1df2-120">passthru</span></span>

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

### <span data-ttu-id="b1df2-121">-UserId</span><span class="sxs-lookup"><span data-stu-id="b1df2-121">-UserId</span></span>
<span data-ttu-id="b1df2-122">Указывает идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="b1df2-122">Specifies the user ID.</span></span>
<span data-ttu-id="b1df2-123">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="b1df2-123">This parameter is required.</span></span>

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

### <span data-ttu-id="b1df2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1df2-124">CommonParameters</span></span>
<span data-ttu-id="b1df2-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b1df2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1df2-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1df2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1df2-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b1df2-127">INPUTS</span></span>

### <span data-ttu-id="b1df2-128">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b1df2-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b1df2-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b1df2-129">System.String</span></span>

### <span data-ttu-id="b1df2-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b1df2-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b1df2-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1df2-131">OUTPUTS</span></span>

### <span data-ttu-id="b1df2-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b1df2-132">System.Boolean</span></span>

## <span data-ttu-id="b1df2-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="b1df2-133">NOTES</span></span>

## <span data-ttu-id="b1df2-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b1df2-134">RELATED LINKS</span></span>

[<span data-ttu-id="b1df2-135">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="b1df2-135">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="b1df2-136">Remove-AzureRmApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="b1df2-136">Remove-AzureRmApiManagementUserFromGroup</span></span>](./Remove-AzureRmApiManagementUserFromGroup.md)


