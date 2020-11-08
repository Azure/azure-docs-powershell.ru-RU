---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementuserfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
ms.openlocfilehash: 220af172efa397de2fc0fafa7597c2b6e29dae60
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235130"
---
# <span data-ttu-id="6191d-101">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="6191d-101">Remove-AzApiManagementUserFromGroup</span></span>

## <span data-ttu-id="6191d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6191d-102">SYNOPSIS</span></span>
<span data-ttu-id="6191d-103">Удаление пользователя из группы.</span><span class="sxs-lookup"><span data-stu-id="6191d-103">Removes a user from a group.</span></span>

## <span data-ttu-id="6191d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6191d-104">SYNTAX</span></span>

```
Remove-AzApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6191d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6191d-105">DESCRIPTION</span></span>
<span data-ttu-id="6191d-106">Командлет **Remove-AzApiManagementUserFromGroup** удаляет пользователя из существующей группы.</span><span class="sxs-lookup"><span data-stu-id="6191d-106">The **Remove-AzApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="6191d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6191d-107">EXAMPLES</span></span>

### <span data-ttu-id="6191d-108">Пример 1: Удаление пользователя из группы</span><span class="sxs-lookup"><span data-stu-id="6191d-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="6191d-109">Эта команда удаляет пользователя из группы.</span><span class="sxs-lookup"><span data-stu-id="6191d-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="6191d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6191d-110">PARAMETERS</span></span>

### <span data-ttu-id="6191d-111">-Context</span><span class="sxs-lookup"><span data-stu-id="6191d-111">-Context</span></span>
<span data-ttu-id="6191d-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="6191d-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="6191d-113">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="6191d-113">This parameter is required.</span></span>

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

### <span data-ttu-id="6191d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6191d-114">-DefaultProfile</span></span>
<span data-ttu-id="6191d-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6191d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6191d-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="6191d-116">-GroupId</span></span>
<span data-ttu-id="6191d-117">Указывает идентификатор группы, из которой нужно удалить пользователя.</span><span class="sxs-lookup"><span data-stu-id="6191d-117">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="6191d-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6191d-118">-PassThru</span></span>
<span data-ttu-id="6191d-119">Указывает на то, что этот командлет возвращает значение $True, если оно прошло успешно, или значение $False, в противном случае.</span><span class="sxs-lookup"><span data-stu-id="6191d-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="6191d-120">-UserId</span><span class="sxs-lookup"><span data-stu-id="6191d-120">-UserId</span></span>
<span data-ttu-id="6191d-121">Указывает идентификатор пользователя, который нужно удалить из группы.</span><span class="sxs-lookup"><span data-stu-id="6191d-121">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="6191d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6191d-122">CommonParameters</span></span>
<span data-ttu-id="6191d-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6191d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6191d-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6191d-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6191d-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6191d-125">INPUTS</span></span>

### <span data-ttu-id="6191d-126">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6191d-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6191d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="6191d-127">System.String</span></span>

### <span data-ttu-id="6191d-128">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6191d-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6191d-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6191d-129">OUTPUTS</span></span>

### <span data-ttu-id="6191d-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6191d-130">System.Boolean</span></span>

## <span data-ttu-id="6191d-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="6191d-131">NOTES</span></span>

## <span data-ttu-id="6191d-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6191d-132">RELATED LINKS</span></span>

[<span data-ttu-id="6191d-133">Add-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="6191d-133">Add-AzApiManagementUserToGroup</span></span>](./Add-AzApiManagementUserToGroup.md)

[<span data-ttu-id="6191d-134">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="6191d-134">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


