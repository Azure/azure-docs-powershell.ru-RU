---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationAzureActiveDirectoryApp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
ms.openlocfilehash: 8eec47c703290047b51ce38e97391500a9f27d74
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100228684"
---
# <span data-ttu-id="ae29c-101">New-AzDataMigrationAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="ae29c-101">New-AzDataMigrationAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="ae29c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae29c-102">SYNOPSIS</span></span>
<span data-ttu-id="ae29c-103">Создайте сведения о приложении DataMigration Azure ActiveDirectory для нового экземпляра.</span><span class="sxs-lookup"><span data-stu-id="ae29c-103">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="ae29c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ae29c-104">SYNTAX</span></span>

```
New-AzDataMigrationAzureActiveDirectoryApp -ApplicationId <String> -AppKey <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae29c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae29c-105">DESCRIPTION</span></span>
<span data-ttu-id="ae29c-106">Создайте сведения о приложении DataMigration Azure ActiveDirectory для нового экземпляра.</span><span class="sxs-lookup"><span data-stu-id="ae29c-106">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="ae29c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ae29c-107">EXAMPLES</span></span>

### <span data-ttu-id="ae29c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ae29c-108">Example 1</span></span>
```powershell
PS C:\> $secpasswd = ConvertTo-SecureString "Your Secret Key Here" -AsPlainText -Force
C:\> New-AzDmsAadApp -ApplicationId "Your AppId/Service Principal ID here" -AppKey $secpasswd
```
<span data-ttu-id="ae29c-109">ApplicationId: "Your AppId/Service Principal Id here" AppKey : System.Security.SecureString TenantId : "Tenant Id"</span><span class="sxs-lookup"><span data-stu-id="ae29c-109">ApplicationId : "Your AppId/Service Principal Id here" AppKey        : System.Security.SecureString TenantId      : "Tenant Id"</span></span>

## <span data-ttu-id="ae29c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae29c-110">PARAMETERS</span></span>

### <span data-ttu-id="ae29c-111">-AppKey</span><span class="sxs-lookup"><span data-stu-id="ae29c-111">-AppKey</span></span>
<span data-ttu-id="ae29c-112">Ключ Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="ae29c-112">Azure Active Directory Key</span></span>

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

### <span data-ttu-id="ae29c-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="ae29c-113">-ApplicationId</span></span>
<span data-ttu-id="ae29c-114">Azure Active Directory Application Id</span><span class="sxs-lookup"><span data-stu-id="ae29c-114">Azure Active Directory Application Id</span></span>

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

### <span data-ttu-id="ae29c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae29c-115">-DefaultProfile</span></span>
<span data-ttu-id="ae29c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ae29c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae29c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae29c-117">CommonParameters</span></span>
<span data-ttu-id="ae29c-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae29c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ae29c-119">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae29c-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae29c-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ae29c-120">INPUTS</span></span>

### <span data-ttu-id="ae29c-121">Нет</span><span class="sxs-lookup"><span data-stu-id="ae29c-121">None</span></span>

## <span data-ttu-id="ae29c-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ae29c-122">OUTPUTS</span></span>

### <span data-ttu-id="ae29c-123">Microsoft.Azure.Commands.DataMigration.Models.PSAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="ae29c-123">Microsoft.Azure.Commands.DataMigration.Models.PSAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="ae29c-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ae29c-124">NOTES</span></span>

## <span data-ttu-id="ae29c-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ae29c-125">RELATED LINKS</span></span>
