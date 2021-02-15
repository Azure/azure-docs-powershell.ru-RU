---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementuserfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
ms.openlocfilehash: 220af172efa397de2fc0fafa7597c2b6e29dae60
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100231228"
---
# <span data-ttu-id="b367c-101">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="b367c-101">Remove-AzApiManagementUserFromGroup</span></span>

## <span data-ttu-id="b367c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b367c-102">SYNOPSIS</span></span>
<span data-ttu-id="b367c-103">Удаляет пользователя из группы.</span><span class="sxs-lookup"><span data-stu-id="b367c-103">Removes a user from a group.</span></span>

## <span data-ttu-id="b367c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b367c-104">SYNTAX</span></span>

```
Remove-AzApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b367c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b367c-105">DESCRIPTION</span></span>
<span data-ttu-id="b367c-106">Для удаления пользователя из существующей группы будет использовать cmdlet **Remove-AzApiManagementUserFromGroup.**</span><span class="sxs-lookup"><span data-stu-id="b367c-106">The **Remove-AzApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="b367c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b367c-107">EXAMPLES</span></span>

### <span data-ttu-id="b367c-108">Пример 1. Удаление пользователя из группы</span><span class="sxs-lookup"><span data-stu-id="b367c-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="b367c-109">Эта команда удаляет пользователя из группы.</span><span class="sxs-lookup"><span data-stu-id="b367c-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="b367c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b367c-110">PARAMETERS</span></span>

### <span data-ttu-id="b367c-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="b367c-111">-Context</span></span>
<span data-ttu-id="b367c-112">Указывает объект **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="b367c-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="b367c-113">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="b367c-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b367c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b367c-114">-DefaultProfile</span></span>
<span data-ttu-id="b367c-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b367c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b367c-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="b367c-116">-GroupId</span></span>
<span data-ttu-id="b367c-117">Определяет ИД группы, из которой нужно удалить пользователя.</span><span class="sxs-lookup"><span data-stu-id="b367c-117">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="b367c-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b367c-118">-PassThru</span></span>
<span data-ttu-id="b367c-119">Указывает на то, что этот $True возвращает значение $True, если он успешно, или значение $False в противном случае.</span><span class="sxs-lookup"><span data-stu-id="b367c-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="b367c-120">-UserId</span><span class="sxs-lookup"><span data-stu-id="b367c-120">-UserId</span></span>
<span data-ttu-id="b367c-121">Определяет ИД пользователя, который нужно удалить из группы.</span><span class="sxs-lookup"><span data-stu-id="b367c-121">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="b367c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b367c-122">CommonParameters</span></span>
<span data-ttu-id="b367c-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b367c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b367c-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b367c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b367c-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b367c-125">INPUTS</span></span>

### <span data-ttu-id="b367c-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b367c-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b367c-127">System.String</span><span class="sxs-lookup"><span data-stu-id="b367c-127">System.String</span></span>

### <span data-ttu-id="b367c-128">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b367c-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b367c-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b367c-129">OUTPUTS</span></span>

### <span data-ttu-id="b367c-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b367c-130">System.Boolean</span></span>

## <span data-ttu-id="b367c-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b367c-131">NOTES</span></span>

## <span data-ttu-id="b367c-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b367c-132">RELATED LINKS</span></span>

[<span data-ttu-id="b367c-133">Add-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="b367c-133">Add-AzApiManagementUserToGroup</span></span>](./Add-AzApiManagementUserToGroup.md)

[<span data-ttu-id="b367c-134">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="b367c-134">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


