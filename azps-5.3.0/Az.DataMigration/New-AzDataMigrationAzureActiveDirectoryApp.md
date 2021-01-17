---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationAzureActiveDirectoryApp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
ms.openlocfilehash: 8eec47c703290047b51ce38e97391500a9f27d74
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426548"
---
# <span data-ttu-id="f1b78-101">New-AzDataMigrationAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="f1b78-101">New-AzDataMigrationAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="f1b78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1b78-102">SYNOPSIS</span></span>
<span data-ttu-id="f1b78-103">Создайте сведения о приложении DataMigration Azure ActiveDirectory для нового экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f1b78-103">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="f1b78-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f1b78-104">SYNTAX</span></span>

```
New-AzDataMigrationAzureActiveDirectoryApp -ApplicationId <String> -AppKey <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1b78-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1b78-105">DESCRIPTION</span></span>
<span data-ttu-id="f1b78-106">Создайте сведения о приложении DataMigration Azure ActiveDirectory для нового экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f1b78-106">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="f1b78-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f1b78-107">EXAMPLES</span></span>

### <span data-ttu-id="f1b78-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f1b78-108">Example 1</span></span>
```powershell
PS C:\> $secpasswd = ConvertTo-SecureString "Your Secret Key Here" -AsPlainText -Force
C:\> New-AzDmsAadApp -ApplicationId "Your AppId/Service Principal ID here" -AppKey $secpasswd
```
<span data-ttu-id="f1b78-109">ApplicationId: "Your AppId/Service Principal Id here" AppKey : System.Security.SecureString TenantId : "Tenant Id"</span><span class="sxs-lookup"><span data-stu-id="f1b78-109">ApplicationId : "Your AppId/Service Principal Id here" AppKey        : System.Security.SecureString TenantId      : "Tenant Id"</span></span>

## <span data-ttu-id="f1b78-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1b78-110">PARAMETERS</span></span>

### <span data-ttu-id="f1b78-111">-AppKey</span><span class="sxs-lookup"><span data-stu-id="f1b78-111">-AppKey</span></span>
<span data-ttu-id="f1b78-112">Ключ Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="f1b78-112">Azure Active Directory Key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: Key

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b78-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="f1b78-113">-ApplicationId</span></span>
<span data-ttu-id="f1b78-114">Azure Active Directory Application Id</span><span class="sxs-lookup"><span data-stu-id="f1b78-114">Azure Active Directory Application Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b78-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1b78-115">-DefaultProfile</span></span>
<span data-ttu-id="f1b78-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f1b78-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1b78-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1b78-117">CommonParameters</span></span>
<span data-ttu-id="f1b78-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1b78-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f1b78-119">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1b78-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1b78-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f1b78-120">INPUTS</span></span>

### <span data-ttu-id="f1b78-121">Нет</span><span class="sxs-lookup"><span data-stu-id="f1b78-121">None</span></span>

## <span data-ttu-id="f1b78-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f1b78-122">OUTPUTS</span></span>

### <span data-ttu-id="f1b78-123">Microsoft.Azure.Commands.DataMigration.Models.PSAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="f1b78-123">Microsoft.Azure.Commands.DataMigration.Models.PSAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="f1b78-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f1b78-124">NOTES</span></span>

## <span data-ttu-id="f1b78-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f1b78-125">RELATED LINKS</span></span>
