---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azmanagedhsmroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmRoleDefinition.md
ms.openlocfilehash: 60ba6fbf57fa9e1ac9e25a913fb9755902b56ddd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245307"
---
# <span data-ttu-id="b9fb6-101">Get-AzManagedHsmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b9fb6-101">Get-AzManagedHsmRoleDefinition</span></span>

## <span data-ttu-id="b9fb6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b9fb6-102">SYNOPSIS</span></span>
<span data-ttu-id="b9fb6-103">Определение ролей для заданного управляемого HSM-файла в заданной области.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-103">List role definitions of a given managed HSM at a given scope.</span></span>

## <span data-ttu-id="b9fb6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b9fb6-104">SYNTAX</span></span>

### <span data-ttu-id="b9fb6-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b9fb6-105">Interactive (Default)</span></span>
```
Get-AzManagedHsmRoleDefinition [-HsmName] <String> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b9fb6-106">ByName</span><span class="sxs-lookup"><span data-stu-id="b9fb6-106">ByName</span></span>
```
Get-AzManagedHsmRoleDefinition [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9fb6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9fb6-107">DESCRIPTION</span></span>
<span data-ttu-id="b9fb6-108">Определение ролей для заданного управляемого HSM-файла в заданной области.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-108">List role definitions of a given managed HSM at a given scope.</span></span>

## <span data-ttu-id="b9fb6-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b9fb6-109">EXAMPLES</span></span>

### <span data-ttu-id="b9fb6-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b9fb6-110">Example 1</span></span>
```powershell
PS C:\> Get-AzManagedHsmRoleDefinition -HsmName myHsm -Scope "/keys"

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

<span data-ttu-id="b9fb6-111">В примере перечислены все роли в области "/Keys".</span><span class="sxs-lookup"><span data-stu-id="b9fb6-111">The example lists all the roles at "/keys" scope.</span></span>

### <span data-ttu-id="b9fb6-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b9fb6-112">Example 2</span></span>
```powershell
PS C:\> $backupRole = Get-AzManagedHsmRoleDefinition -HsmName myHsm -RoleDefinitionName "managed hsm backup"

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

<span data-ttu-id="b9fb6-113">В примере возвращается роль "управляемый резервный код HSM" и проверяются ее разрешения.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-113">The example gets the "Managed HSM Backup" role and inspects its permissions.</span></span>

## <span data-ttu-id="b9fb6-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b9fb6-114">PARAMETERS</span></span>

### <span data-ttu-id="b9fb6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9fb6-115">-DefaultProfile</span></span>
<span data-ttu-id="b9fb6-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9fb6-117">-HsmName</span><span class="sxs-lookup"><span data-stu-id="b9fb6-117">-HsmName</span></span>
<span data-ttu-id="b9fb6-118">Имя HSM.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-118">Name of the HSM.</span></span>

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

### <span data-ttu-id="b9fb6-119">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="b9fb6-119">-RoleDefinitionName</span></span>
<span data-ttu-id="b9fb6-120">Имя определения роли, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-120">Name of the role definition to get.</span></span>

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

### <span data-ttu-id="b9fb6-121">-Scope</span><span class="sxs-lookup"><span data-stu-id="b9fb6-121">-Scope</span></span>
<span data-ttu-id="b9fb6-122">Область, к которой относится назначение роли или определение (например, "/" или "/Keys" или "/keys/{keyName}").</span><span class="sxs-lookup"><span data-stu-id="b9fb6-122">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="b9fb6-123">"/" используется, если опущен.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-123">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="b9fb6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9fb6-124">CommonParameters</span></span>
<span data-ttu-id="b9fb6-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b9fb6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9fb6-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9fb6-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9fb6-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b9fb6-127">INPUTS</span></span>

### <span data-ttu-id="b9fb6-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="b9fb6-128">None</span></span>

## <span data-ttu-id="b9fb6-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9fb6-129">OUTPUTS</span></span>

### <span data-ttu-id="b9fb6-130">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b9fb6-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleDefinition</span></span>

## <span data-ttu-id="b9fb6-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="b9fb6-131">NOTES</span></span>

## <span data-ttu-id="b9fb6-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b9fb6-132">RELATED LINKS</span></span>
