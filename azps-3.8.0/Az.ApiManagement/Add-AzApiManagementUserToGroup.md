---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementusertogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementUserToGroup.md
ms.openlocfilehash: 27e6be451d6141e322c47b2a84a28baf115839ef
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073944"
---
# <span data-ttu-id="8be69-101">Add-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="8be69-101">Add-AzApiManagementUserToGroup</span></span>

## <span data-ttu-id="8be69-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8be69-102">SYNOPSIS</span></span>
<span data-ttu-id="8be69-103">Добавляет пользователя в группу.</span><span class="sxs-lookup"><span data-stu-id="8be69-103">Adds a user to a group.</span></span>

## <span data-ttu-id="8be69-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8be69-104">SYNTAX</span></span>

```
Add-AzApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8be69-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8be69-105">DESCRIPTION</span></span>
<span data-ttu-id="8be69-106">Командлет **Add-AzApiManagementUserToGroup** добавляет пользователя в группу.</span><span class="sxs-lookup"><span data-stu-id="8be69-106">The **Add-AzApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="8be69-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8be69-107">EXAMPLES</span></span>

### <span data-ttu-id="8be69-108">Пример 1: Добавление пользователя в группу</span><span class="sxs-lookup"><span data-stu-id="8be69-108">Example 1: Add a user to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="8be69-109">Эта команда добавляет существующего пользователя в существующую группу.</span><span class="sxs-lookup"><span data-stu-id="8be69-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="8be69-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8be69-110">PARAMETERS</span></span>

### <span data-ttu-id="8be69-111">-Context</span><span class="sxs-lookup"><span data-stu-id="8be69-111">-Context</span></span>
<span data-ttu-id="8be69-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="8be69-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="8be69-113">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="8be69-113">This parameter is required.</span></span>

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

### <span data-ttu-id="8be69-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8be69-114">-DefaultProfile</span></span>
<span data-ttu-id="8be69-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8be69-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8be69-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="8be69-116">-GroupId</span></span>
<span data-ttu-id="8be69-117">Указывает код группы.</span><span class="sxs-lookup"><span data-stu-id="8be69-117">Specifies the group ID.</span></span>
<span data-ttu-id="8be69-118">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="8be69-118">This parameter is required.</span></span>

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

### <span data-ttu-id="8be69-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8be69-119">-PassThru</span></span>
<span data-ttu-id="8be69-120">PassThru</span><span class="sxs-lookup"><span data-stu-id="8be69-120">passthru</span></span>

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

### <span data-ttu-id="8be69-121">-UserId</span><span class="sxs-lookup"><span data-stu-id="8be69-121">-UserId</span></span>
<span data-ttu-id="8be69-122">Указывает идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="8be69-122">Specifies the user ID.</span></span>
<span data-ttu-id="8be69-123">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="8be69-123">This parameter is required.</span></span>

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

### <span data-ttu-id="8be69-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8be69-124">CommonParameters</span></span>
<span data-ttu-id="8be69-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8be69-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8be69-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8be69-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8be69-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8be69-127">INPUTS</span></span>

### <span data-ttu-id="8be69-128">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8be69-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8be69-129">System. String</span><span class="sxs-lookup"><span data-stu-id="8be69-129">System.String</span></span>

### <span data-ttu-id="8be69-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8be69-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8be69-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8be69-131">OUTPUTS</span></span>

### <span data-ttu-id="8be69-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8be69-132">System.Boolean</span></span>

## <span data-ttu-id="8be69-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="8be69-133">NOTES</span></span>

## <span data-ttu-id="8be69-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8be69-134">RELATED LINKS</span></span>

[<span data-ttu-id="8be69-135">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="8be69-135">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="8be69-136">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="8be69-136">Remove-AzApiManagementUserFromGroup</span></span>](./Remove-AzApiManagementUserFromGroup.md)


