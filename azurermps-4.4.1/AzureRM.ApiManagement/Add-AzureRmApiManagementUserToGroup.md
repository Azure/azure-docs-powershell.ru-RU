---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
ms.openlocfilehash: d405dc21719abc1aec5767f4d1b89a938b79eaf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560595"
---
# <span data-ttu-id="f3d49-101">Add-AzureRmApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="f3d49-101">Add-AzureRmApiManagementUserToGroup</span></span>

## <span data-ttu-id="f3d49-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f3d49-102">SYNOPSIS</span></span>
<span data-ttu-id="f3d49-103">Добавляет пользователя в группу.</span><span class="sxs-lookup"><span data-stu-id="f3d49-103">Adds a user to a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3d49-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f3d49-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3d49-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3d49-105">DESCRIPTION</span></span>
<span data-ttu-id="f3d49-106">Командлет **Add-AzureRmApiManagementUserToGroup** добавляет пользователя в группу.</span><span class="sxs-lookup"><span data-stu-id="f3d49-106">The **Add-AzureRmApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="f3d49-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f3d49-107">EXAMPLES</span></span>

### <span data-ttu-id="f3d49-108">Пример 1: Добавление пользователя в группу</span><span class="sxs-lookup"><span data-stu-id="f3d49-108">Example 1: Add a user to a group</span></span>
```
PS C:\>Add-AzureRmApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="f3d49-109">Эта команда добавляет существующего пользователя в существующую группу.</span><span class="sxs-lookup"><span data-stu-id="f3d49-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="f3d49-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f3d49-110">PARAMETERS</span></span>

### <span data-ttu-id="f3d49-111">-Context</span><span class="sxs-lookup"><span data-stu-id="f3d49-111">-Context</span></span>
<span data-ttu-id="f3d49-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="f3d49-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="f3d49-113">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="f3d49-113">This parameter is required.</span></span>

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

### <span data-ttu-id="f3d49-114">-GroupId</span><span class="sxs-lookup"><span data-stu-id="f3d49-114">-GroupId</span></span>
<span data-ttu-id="f3d49-115">Указывает код группы.</span><span class="sxs-lookup"><span data-stu-id="f3d49-115">Specifies the group ID.</span></span>
<span data-ttu-id="f3d49-116">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="f3d49-116">This parameter is required.</span></span>

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

### <span data-ttu-id="f3d49-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3d49-117">-PassThru</span></span>
<span data-ttu-id="f3d49-118">PassThru</span><span class="sxs-lookup"><span data-stu-id="f3d49-118">passthru</span></span>

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

### <span data-ttu-id="f3d49-119">-UserId</span><span class="sxs-lookup"><span data-stu-id="f3d49-119">-UserId</span></span>
<span data-ttu-id="f3d49-120">Указывает идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="f3d49-120">Specifies the user ID.</span></span>
<span data-ttu-id="f3d49-121">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="f3d49-121">This parameter is required.</span></span>

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

### <span data-ttu-id="f3d49-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3d49-122">-DefaultProfile</span></span>
<span data-ttu-id="f3d49-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f3d49-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3d49-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3d49-124">CommonParameters</span></span>
<span data-ttu-id="f3d49-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f3d49-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3d49-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3d49-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3d49-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f3d49-127">INPUTS</span></span>

## <span data-ttu-id="f3d49-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3d49-128">OUTPUTS</span></span>

### <span data-ttu-id="f3d49-129">Значением</span><span class="sxs-lookup"><span data-stu-id="f3d49-129">Boolean</span></span>

## <span data-ttu-id="f3d49-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="f3d49-130">NOTES</span></span>

## <span data-ttu-id="f3d49-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f3d49-131">RELATED LINKS</span></span>

[<span data-ttu-id="f3d49-132">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f3d49-132">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="f3d49-133">Remove-AzureRmApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="f3d49-133">Remove-AzureRmApiManagementUserFromGroup</span></span>](./Remove-AzureRmApiManagementUserFromGroup.md)


