---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementuserfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
ms.openlocfilehash: 73d21a78fd71a677c03e52e131abb7050d71fffc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727963"
---
# <span data-ttu-id="72da5-101">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="72da5-101">Remove-AzApiManagementUserFromGroup</span></span>

## <span data-ttu-id="72da5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="72da5-102">SYNOPSIS</span></span>
<span data-ttu-id="72da5-103">Удаление пользователя из группы.</span><span class="sxs-lookup"><span data-stu-id="72da5-103">Removes a user from a group.</span></span>

## <span data-ttu-id="72da5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="72da5-104">SYNTAX</span></span>

```
Remove-AzApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72da5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="72da5-105">DESCRIPTION</span></span>
<span data-ttu-id="72da5-106">Командлет **Remove-AzApiManagementUserFromGroup** удаляет пользователя из существующей группы.</span><span class="sxs-lookup"><span data-stu-id="72da5-106">The **Remove-AzApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="72da5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="72da5-107">EXAMPLES</span></span>

### <span data-ttu-id="72da5-108">Пример 1: Удаление пользователя из группы</span><span class="sxs-lookup"><span data-stu-id="72da5-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="72da5-109">Эта команда удаляет пользователя из группы.</span><span class="sxs-lookup"><span data-stu-id="72da5-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="72da5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="72da5-110">PARAMETERS</span></span>

### <span data-ttu-id="72da5-111">-Context</span><span class="sxs-lookup"><span data-stu-id="72da5-111">-Context</span></span>
<span data-ttu-id="72da5-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="72da5-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="72da5-113">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="72da5-113">This parameter is required.</span></span>

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

### <span data-ttu-id="72da5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72da5-114">-DefaultProfile</span></span>
<span data-ttu-id="72da5-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="72da5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72da5-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="72da5-116">-GroupId</span></span>
<span data-ttu-id="72da5-117">Указывает идентификатор группы, из которой нужно удалить пользователя.</span><span class="sxs-lookup"><span data-stu-id="72da5-117">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="72da5-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="72da5-118">-PassThru</span></span>
<span data-ttu-id="72da5-119">Указывает на то, что этот командлет возвращает значение $True, если оно прошло успешно, или значение $False, в противном случае.</span><span class="sxs-lookup"><span data-stu-id="72da5-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="72da5-120">-UserId</span><span class="sxs-lookup"><span data-stu-id="72da5-120">-UserId</span></span>
<span data-ttu-id="72da5-121">Указывает идентификатор пользователя, который нужно удалить из группы.</span><span class="sxs-lookup"><span data-stu-id="72da5-121">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="72da5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72da5-122">CommonParameters</span></span>
<span data-ttu-id="72da5-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="72da5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72da5-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72da5-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72da5-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="72da5-125">INPUTS</span></span>

### <span data-ttu-id="72da5-126">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="72da5-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="72da5-127">System. String</span><span class="sxs-lookup"><span data-stu-id="72da5-127">System.String</span></span>

### <span data-ttu-id="72da5-128">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="72da5-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="72da5-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="72da5-129">OUTPUTS</span></span>

### <span data-ttu-id="72da5-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="72da5-130">System.Boolean</span></span>

## <span data-ttu-id="72da5-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="72da5-131">NOTES</span></span>

## <span data-ttu-id="72da5-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="72da5-132">RELATED LINKS</span></span>

[<span data-ttu-id="72da5-133">Add-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="72da5-133">Add-AzApiManagementUserToGroup</span></span>](./Add-AzApiManagementUserToGroup.md)

[<span data-ttu-id="72da5-134">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="72da5-134">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


