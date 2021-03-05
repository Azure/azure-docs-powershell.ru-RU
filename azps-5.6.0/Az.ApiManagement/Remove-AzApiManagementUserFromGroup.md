---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementuserfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
ms.openlocfilehash: 03073dc6116595c93b2c25d30b38c5467482903c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010952"
---
# <span data-ttu-id="eaba5-101">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="eaba5-101">Remove-AzApiManagementUserFromGroup</span></span>

## <span data-ttu-id="eaba5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eaba5-102">SYNOPSIS</span></span>
<span data-ttu-id="eaba5-103">Удаляет пользователя из группы.</span><span class="sxs-lookup"><span data-stu-id="eaba5-103">Removes a user from a group.</span></span>

## <span data-ttu-id="eaba5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="eaba5-104">SYNTAX</span></span>

```
Remove-AzApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eaba5-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eaba5-105">DESCRIPTION</span></span>
<span data-ttu-id="eaba5-106">Для удаления пользователя из существующей группы будет использовать cmdlet **Remove-AzApiManagementUserFromGroup.**</span><span class="sxs-lookup"><span data-stu-id="eaba5-106">The **Remove-AzApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="eaba5-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="eaba5-107">EXAMPLES</span></span>

### <span data-ttu-id="eaba5-108">Пример 1. Удаление пользователя из группы</span><span class="sxs-lookup"><span data-stu-id="eaba5-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="eaba5-109">Эта команда удаляет пользователя из группы.</span><span class="sxs-lookup"><span data-stu-id="eaba5-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="eaba5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eaba5-110">PARAMETERS</span></span>

### <span data-ttu-id="eaba5-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="eaba5-111">-Context</span></span>
<span data-ttu-id="eaba5-112">Указывает объект **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="eaba5-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="eaba5-113">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="eaba5-113">This parameter is required.</span></span>

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

### <span data-ttu-id="eaba5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaba5-114">-DefaultProfile</span></span>
<span data-ttu-id="eaba5-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eaba5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eaba5-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="eaba5-116">-GroupId</span></span>
<span data-ttu-id="eaba5-117">Определяет ИД группы, из которой нужно удалить пользователя.</span><span class="sxs-lookup"><span data-stu-id="eaba5-117">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="eaba5-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eaba5-118">-PassThru</span></span>
<span data-ttu-id="eaba5-119">Указывает на то, что этот $True возвращает значение $True, если он успешно, или значение $False в противном случае.</span><span class="sxs-lookup"><span data-stu-id="eaba5-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="eaba5-120">-UserId</span><span class="sxs-lookup"><span data-stu-id="eaba5-120">-UserId</span></span>
<span data-ttu-id="eaba5-121">Определяет ИД пользователя, который нужно удалить из группы.</span><span class="sxs-lookup"><span data-stu-id="eaba5-121">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="eaba5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaba5-122">CommonParameters</span></span>
<span data-ttu-id="eaba5-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eaba5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaba5-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eaba5-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaba5-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eaba5-125">INPUTS</span></span>

### <span data-ttu-id="eaba5-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="eaba5-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="eaba5-127">System.String</span><span class="sxs-lookup"><span data-stu-id="eaba5-127">System.String</span></span>

### <span data-ttu-id="eaba5-128">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="eaba5-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="eaba5-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="eaba5-129">OUTPUTS</span></span>

### <span data-ttu-id="eaba5-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="eaba5-130">System.Boolean</span></span>

## <span data-ttu-id="eaba5-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="eaba5-131">NOTES</span></span>

## <span data-ttu-id="eaba5-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eaba5-132">RELATED LINKS</span></span>

[<span data-ttu-id="eaba5-133">Add-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="eaba5-133">Add-AzApiManagementUserToGroup</span></span>](./Add-AzApiManagementUserToGroup.md)

[<span data-ttu-id="eaba5-134">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="eaba5-134">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


