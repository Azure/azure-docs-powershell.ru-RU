---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationAzureActiveDirectoryApp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
ms.openlocfilehash: 8eec47c703290047b51ce38e97391500a9f27d74
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236761"
---
# <span data-ttu-id="7fa3e-101">New-AzDataMigrationAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="7fa3e-101">New-AzDataMigrationAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="7fa3e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7fa3e-102">SYNOPSIS</span></span>
<span data-ttu-id="7fa3e-103">Создайте новые сведения о приложении Azure ActiveDirectory для миграции экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7fa3e-103">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="7fa3e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7fa3e-104">SYNTAX</span></span>

```
New-AzDataMigrationAzureActiveDirectoryApp -ApplicationId <String> -AppKey <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fa3e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7fa3e-105">DESCRIPTION</span></span>
<span data-ttu-id="7fa3e-106">Создайте новые сведения о приложении Azure ActiveDirectory для миграции экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7fa3e-106">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="7fa3e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7fa3e-107">EXAMPLES</span></span>

### <span data-ttu-id="7fa3e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7fa3e-108">Example 1</span></span>
```powershell
PS C:\> $secpasswd = ConvertTo-SecureString "Your Secret Key Here" -AsPlainText -Force
C:\> New-AzDmsAadApp -ApplicationId "Your AppId/Service Principal ID here" -AppKey $secpasswd
```
<span data-ttu-id="7fa3e-109">ApplicationId: "свои AppId/Service ID участника здесь" AppKey: System. Security. SecureString TenantId: "ИД клиента"</span><span class="sxs-lookup"><span data-stu-id="7fa3e-109">ApplicationId : "Your AppId/Service Principal Id here" AppKey        : System.Security.SecureString TenantId      : "Tenant Id"</span></span>

## <span data-ttu-id="7fa3e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7fa3e-110">PARAMETERS</span></span>

### <span data-ttu-id="7fa3e-111">-AppKey</span><span class="sxs-lookup"><span data-stu-id="7fa3e-111">-AppKey</span></span>
<span data-ttu-id="7fa3e-112">Ключ Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="7fa3e-112">Azure Active Directory Key</span></span>

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

### <span data-ttu-id="7fa3e-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="7fa3e-113">-ApplicationId</span></span>
<span data-ttu-id="7fa3e-114">Идентификатор приложения Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="7fa3e-114">Azure Active Directory Application Id</span></span>

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

### <span data-ttu-id="7fa3e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fa3e-115">-DefaultProfile</span></span>
<span data-ttu-id="7fa3e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7fa3e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fa3e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fa3e-117">CommonParameters</span></span>
<span data-ttu-id="7fa3e-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7fa3e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7fa3e-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fa3e-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fa3e-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7fa3e-120">INPUTS</span></span>

### <span data-ttu-id="7fa3e-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="7fa3e-121">None</span></span>

## <span data-ttu-id="7fa3e-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7fa3e-122">OUTPUTS</span></span>

### <span data-ttu-id="7fa3e-123">Microsoft. Azure. Commands. Migration. Models. PSAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="7fa3e-123">Microsoft.Azure.Commands.DataMigration.Models.PSAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="7fa3e-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="7fa3e-124">NOTES</span></span>

## <span data-ttu-id="7fa3e-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7fa3e-125">RELATED LINKS</span></span>