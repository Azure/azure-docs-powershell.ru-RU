---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementusertogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementUserToGroup.md
ms.openlocfilehash: 27e6be451d6141e322c47b2a84a28baf115839ef
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398780"
---
# <span data-ttu-id="d070e-101">Add-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="d070e-101">Add-AzApiManagementUserToGroup</span></span>

## <span data-ttu-id="d070e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d070e-102">SYNOPSIS</span></span>
<span data-ttu-id="d070e-103">Добавляет пользователя в группу.</span><span class="sxs-lookup"><span data-stu-id="d070e-103">Adds a user to a group.</span></span>

## <span data-ttu-id="d070e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d070e-104">SYNTAX</span></span>

```
Add-AzApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d070e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d070e-105">DESCRIPTION</span></span>
<span data-ttu-id="d070e-106">Чтобы добавить пользователя в группу, можно добавить пользователя в группу с учетом выполнения **cmdlet Add-AzApiManagementUserToGroup.**</span><span class="sxs-lookup"><span data-stu-id="d070e-106">The **Add-AzApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="d070e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d070e-107">EXAMPLES</span></span>

### <span data-ttu-id="d070e-108">Пример 1. Добавление пользователя в группу</span><span class="sxs-lookup"><span data-stu-id="d070e-108">Example 1: Add a user to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="d070e-109">Эта команда добавляет существующего пользователя в существующую группу.</span><span class="sxs-lookup"><span data-stu-id="d070e-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="d070e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d070e-110">PARAMETERS</span></span>

### <span data-ttu-id="d070e-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="d070e-111">-Context</span></span>
<span data-ttu-id="d070e-112">Указывает объект **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="d070e-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="d070e-113">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="d070e-113">This parameter is required.</span></span>

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

### <span data-ttu-id="d070e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d070e-114">-DefaultProfile</span></span>
<span data-ttu-id="d070e-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d070e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d070e-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="d070e-116">-GroupId</span></span>
<span data-ttu-id="d070e-117">Определяет ИД группы.</span><span class="sxs-lookup"><span data-stu-id="d070e-117">Specifies the group ID.</span></span>
<span data-ttu-id="d070e-118">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="d070e-118">This parameter is required.</span></span>

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

### <span data-ttu-id="d070e-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d070e-119">-PassThru</span></span>
<span data-ttu-id="d070e-120">passthru</span><span class="sxs-lookup"><span data-stu-id="d070e-120">passthru</span></span>

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

### <span data-ttu-id="d070e-121">-UserId</span><span class="sxs-lookup"><span data-stu-id="d070e-121">-UserId</span></span>
<span data-ttu-id="d070e-122">Определяет ИД пользователя.</span><span class="sxs-lookup"><span data-stu-id="d070e-122">Specifies the user ID.</span></span>
<span data-ttu-id="d070e-123">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="d070e-123">This parameter is required.</span></span>

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

### <span data-ttu-id="d070e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d070e-124">CommonParameters</span></span>
<span data-ttu-id="d070e-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d070e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d070e-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d070e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d070e-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d070e-127">INPUTS</span></span>

### <span data-ttu-id="d070e-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d070e-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d070e-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d070e-129">System.String</span></span>

### <span data-ttu-id="d070e-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d070e-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d070e-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d070e-131">OUTPUTS</span></span>

### <span data-ttu-id="d070e-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d070e-132">System.Boolean</span></span>

## <span data-ttu-id="d070e-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d070e-133">NOTES</span></span>

## <span data-ttu-id="d070e-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d070e-134">RELATED LINKS</span></span>

[<span data-ttu-id="d070e-135">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="d070e-135">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="d070e-136">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="d070e-136">Remove-AzApiManagementUserFromGroup</span></span>](./Remove-AzApiManagementUserFromGroup.md)


