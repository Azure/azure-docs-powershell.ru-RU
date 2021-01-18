---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAutoProvisioningSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAutoProvisioningSetting.md
ms.openlocfilehash: 08631f5705a3a0255c42ac3d146cef45de1b4e56
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517717"
---
# <span data-ttu-id="afb09-101">Get-AzSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="afb09-101">Get-AzSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="afb09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afb09-102">SYNOPSIS</span></span>
<span data-ttu-id="afb09-103">Параметры автоматической установки системы безопасности</span><span class="sxs-lookup"><span data-stu-id="afb09-103">Gets the security automatic provisioning settings</span></span>

## <span data-ttu-id="afb09-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="afb09-104">SYNTAX</span></span>

### <span data-ttu-id="afb09-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="afb09-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAutoProvisioningSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="afb09-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="afb09-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAutoProvisioningSetting -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="afb09-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="afb09-107">ResourceId</span></span>
```
Get-AzSecurityAutoProvisioningSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="afb09-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="afb09-108">DESCRIPTION</span></span>
<span data-ttu-id="afb09-109">Параметры автоматической установки по выбору центра безопасности Azure могут автоматически создать агент безопасности, который будет устанавливаться на ваши VMs.</span><span class="sxs-lookup"><span data-stu-id="afb09-109">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="afb09-110">Агент безопасности будет отслеживать VM-компьютер для создания оповещений системы безопасности и соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="afb09-110">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="afb09-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="afb09-111">EXAMPLES</span></span>

### <span data-ttu-id="afb09-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="afb09-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="afb09-113">Получает параметр автоматической подготовка для подписки</span><span class="sxs-lookup"><span data-stu-id="afb09-113">Gets the auto provisioning setting for the subscription</span></span>

## <span data-ttu-id="afb09-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="afb09-114">PARAMETERS</span></span>

### <span data-ttu-id="afb09-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afb09-115">-DefaultProfile</span></span>
<span data-ttu-id="afb09-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="afb09-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afb09-117">-Name</span><span class="sxs-lookup"><span data-stu-id="afb09-117">-Name</span></span>
<span data-ttu-id="afb09-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="afb09-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afb09-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="afb09-119">-ResourceId</span></span>
<span data-ttu-id="afb09-120">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="afb09-120">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afb09-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afb09-121">CommonParameters</span></span>
<span data-ttu-id="afb09-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afb09-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afb09-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="afb09-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afb09-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="afb09-124">INPUTS</span></span>

### <span data-ttu-id="afb09-125">System.String</span><span class="sxs-lookup"><span data-stu-id="afb09-125">System.String</span></span>

## <span data-ttu-id="afb09-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="afb09-126">OUTPUTS</span></span>

### <span data-ttu-id="afb09-127">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="afb09-127">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="afb09-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="afb09-128">NOTES</span></span>

## <span data-ttu-id="afb09-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="afb09-129">RELATED LINKS</span></span>
