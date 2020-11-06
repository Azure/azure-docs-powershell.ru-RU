---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: CAB32C72-5C16-467E-BC57-749EC49916BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/set-azurermdatalakeanalyticscatalogsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogSecret.md
ms.openlocfilehash: cce57a2437a5e1fa0f440986534a11c1ab6c73ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563579"
---
# <span data-ttu-id="bf428-101">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="bf428-101">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>

## <span data-ttu-id="bf428-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bf428-102">SYNOPSIS</span></span>
<span data-ttu-id="bf428-103">Изменение секрета для каталога Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="bf428-103">Modifies a Data Lake Analytics catalog secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf428-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bf428-104">SYNTAX</span></span>

### <span data-ttu-id="bf428-105">SetByFullUri</span><span class="sxs-lookup"><span data-stu-id="bf428-105">SetByFullUri</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-DatabaseHost] <String> [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf428-106">SetByHostNameAndPort</span><span class="sxs-lookup"><span data-stu-id="bf428-106">SetByHostNameAndPort</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-Uri] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf428-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf428-107">DESCRIPTION</span></span>
<span data-ttu-id="bf428-108">Командлет **Set-AzureRmDataLakeAnalyticsCatalogSecret** изменяет секрет, связанный с каталогом Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="bf428-108">The **Set-AzureRmDataLakeAnalyticsCatalogSecret** cmdlet modifies a secret associated with an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="bf428-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bf428-109">EXAMPLES</span></span>

### <span data-ttu-id="bf428-110">Пример 1: изменение секрета, связанного с учетной записью</span><span class="sxs-lookup"><span data-stu-id="bf428-110">Example 1: Modify the secret associated with an account</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsCatalogSecret -Account "ContosoAdlAccount" -DatabaseName "databaseName" -Secret (Get-Credential) -Host "https://example.contoso.com" -Port 8080
```

<span data-ttu-id="bf428-111">Эта команда задает секретный ключ, связанный с каталогом Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="bf428-111">This command sets the secret associated with a Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="bf428-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bf428-112">PARAMETERS</span></span>

### <span data-ttu-id="bf428-113">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="bf428-113">-Account</span></span>
<span data-ttu-id="bf428-114">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="bf428-114">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf428-115">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="bf428-115">-DatabaseHost</span></span>
<span data-ttu-id="bf428-116">Указывает имя узла для базы данных, с которым связан секрет в формате "mydatabase.contoso.com".</span><span class="sxs-lookup"><span data-stu-id="bf428-116">Specifies the host name for the database the secret is associated with in the format 'mydatabase.contoso.com'.</span></span>

```yaml
Type: String
Parameter Sets: SetByFullUri
Aliases: Host

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf428-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bf428-117">-DatabaseName</span></span>
<span data-ttu-id="bf428-118">Указывает имя базы данных, в которой хранятся секретные секреты.</span><span class="sxs-lookup"><span data-stu-id="bf428-118">Specifies the name of the database holding the secret.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf428-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf428-119">-DefaultProfile</span></span>
<span data-ttu-id="bf428-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bf428-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf428-121">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="bf428-121">-Port</span></span>
<span data-ttu-id="bf428-122">Задает номер порта секрета.</span><span class="sxs-lookup"><span data-stu-id="bf428-122">Specifies the port number of the secret.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByFullUri
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf428-123">-Secret (секретный)</span><span class="sxs-lookup"><span data-stu-id="bf428-123">-Secret</span></span>
<span data-ttu-id="bf428-124">Указывает имя и пароль секрета.</span><span class="sxs-lookup"><span data-stu-id="bf428-124">Specifies the name and password of the secret.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf428-125">-URI</span><span class="sxs-lookup"><span data-stu-id="bf428-125">-Uri</span></span>
<span data-ttu-id="bf428-126">Задает универсальный код ресурса (URI) для секрета.</span><span class="sxs-lookup"><span data-stu-id="bf428-126">Specifies the Uniform Resource Identifier (URI) for the secret.</span></span>

```yaml
Type: Uri
Parameter Sets: SetByHostNameAndPort
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf428-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf428-127">CommonParameters</span></span>
<span data-ttu-id="bf428-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bf428-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf428-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf428-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf428-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bf428-130">INPUTS</span></span>

### <span data-ttu-id="bf428-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="bf428-131">None</span></span>
<span data-ttu-id="bf428-132">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="bf428-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bf428-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf428-133">OUTPUTS</span></span>

### <span data-ttu-id="bf428-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="bf428-134">None</span></span>

## <span data-ttu-id="bf428-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="bf428-135">NOTES</span></span>

## <span data-ttu-id="bf428-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bf428-136">RELATED LINKS</span></span>

[<span data-ttu-id="bf428-137">New-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="bf428-137">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./New-AzureRmDataLakeAnalyticsCatalogSecret.md)

[<span data-ttu-id="bf428-138">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="bf428-138">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Remove-AzureRmDataLakeAnalyticsCatalogSecret.md)


