---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleDefinition.md
ms.openlocfilehash: 6e4f58c355296a281a9ecbef21d7eca754bf41c0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507200"
---
# <span data-ttu-id="706c8-101">Get-AzKeyVaultRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="706c8-101">Get-AzKeyVaultRoleDefinition</span></span>

## <span data-ttu-id="706c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="706c8-102">SYNOPSIS</span></span>
<span data-ttu-id="706c8-103">Определение ролей для управляемых HSM в заданной области.</span><span class="sxs-lookup"><span data-stu-id="706c8-103">List role definitions of a given managed HSM at a given scope.</span></span>

## <span data-ttu-id="706c8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="706c8-104">SYNTAX</span></span>

### <span data-ttu-id="706c8-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="706c8-105">Interactive (Default)</span></span>
```
Get-AzKeyVaultRoleDefinition [-HsmName] <String> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="706c8-106">ByName</span><span class="sxs-lookup"><span data-stu-id="706c8-106">ByName</span></span>
```
Get-AzKeyVaultRoleDefinition [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="706c8-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="706c8-107">DESCRIPTION</span></span>
<span data-ttu-id="706c8-108">Определение ролей для управляемых HSM в заданной области.</span><span class="sxs-lookup"><span data-stu-id="706c8-108">List role definitions of a given managed HSM at a given scope.</span></span>

## <span data-ttu-id="706c8-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="706c8-109">EXAMPLES</span></span>

### <span data-ttu-id="706c8-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="706c8-110">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVaultRoleDefinition -HsmName myHsm -Scope "/keys"

RoleName                              Description Permissions
--------                              ----------- -----------
Managed HSM Administrator                         1 permission(s)
Managed HSM Crypto Officer                        1 permission(s)
Managed HSM Crypto User                           1 permission(s)
Managed HSM Policy Administrator                  1 permission(s)
Managed HSM Crypto Auditor                        1 permission(s)
Managed HSM Crypto Service Encryption             1 permission(s)
Managed HSM Backup                                1 permission(s)
```

<span data-ttu-id="706c8-111">В примере перечислены все роли в области "/keys".</span><span class="sxs-lookup"><span data-stu-id="706c8-111">The example lists all the roles at "/keys" scope.</span></span>

### <span data-ttu-id="706c8-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="706c8-112">Example 2</span></span>
```powershell
PS C:\> $backupRole = Get-AzKeyVaultRoleDefinition -HsmName myHsm -RoleDefinitionName "managed hsm backup"

PS C:\> $backupRole.Permissions

AllowedActions DeniedActions AllowedDataActions DeniedDataActions
-------------- ------------- ------------------ -----------------
0 action(s)    0 action(s)   3 action(s)        0 action(s)

PS C:\> $backupRole.Permissions.AllowedDataActions

Microsoft.KeyVault/managedHsm/backup/start/action
Microsoft.KeyVault/managedHsm/backup/status/action
Microsoft.KeyVault/managedHsm/keys/backup/action

RoleName                              Description Permissions
--------                              ----------- -----------
Managed HSM Administrator                         1 permission(s)
Managed HSM Crypto Officer                        1 permission(s)
Managed HSM Crypto User                           1 permission(s)
Managed HSM Policy Administrator                  1 permission(s)
Managed HSM Crypto Auditor                        1 permission(s)
Managed HSM Crypto Service Encryption             1 permission(s)
Managed HSM Backup                                1 permission(s)
```

<span data-ttu-id="706c8-113">В этом примере получается роль "Управляемое резервное копирование HSM" и проверяется ее разрешения.</span><span class="sxs-lookup"><span data-stu-id="706c8-113">The example gets the "Managed HSM Backup" role and inspects its permissions.</span></span>

## <span data-ttu-id="706c8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="706c8-114">PARAMETERS</span></span>

### <span data-ttu-id="706c8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="706c8-115">-DefaultProfile</span></span>
<span data-ttu-id="706c8-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="706c8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="706c8-117">-HsmName</span><span class="sxs-lookup"><span data-stu-id="706c8-117">-HsmName</span></span>
<span data-ttu-id="706c8-118">Имя HSM.</span><span class="sxs-lookup"><span data-stu-id="706c8-118">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="706c8-119">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="706c8-119">-RoleDefinitionName</span></span>
<span data-ttu-id="706c8-120">Имя определения роли, которое нужно получить.</span><span class="sxs-lookup"><span data-stu-id="706c8-120">Name of the role definition to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: RoleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="706c8-121">-Scope</span><span class="sxs-lookup"><span data-stu-id="706c8-121">-Scope</span></span>
<span data-ttu-id="706c8-122">Область применения назначения роли или определения, например "/", "/" или "/keys" или "/keys/{keyName}".</span><span class="sxs-lookup"><span data-stu-id="706c8-122">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="706c8-123">"/" используется в опущении.</span><span class="sxs-lookup"><span data-stu-id="706c8-123">'/' is used when omitted.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="706c8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="706c8-124">CommonParameters</span></span>
<span data-ttu-id="706c8-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="706c8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="706c8-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="706c8-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="706c8-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="706c8-127">INPUTS</span></span>

### <span data-ttu-id="706c8-128">Нет</span><span class="sxs-lookup"><span data-stu-id="706c8-128">None</span></span>

## <span data-ttu-id="706c8-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="706c8-129">OUTPUTS</span></span>

### <span data-ttu-id="706c8-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="706c8-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleDefinition</span></span>

## <span data-ttu-id="706c8-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="706c8-131">NOTES</span></span>

## <span data-ttu-id="706c8-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="706c8-132">RELATED LINKS</span></span>
